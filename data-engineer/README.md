# The challenge (Data Engineer)

The goal of the challenge is to have a tool that is able to stream data from 
[kafka](http://kafka.apache.org/) and count unique things within this data. The simplest use case is
that we want to calculate unique users per minute, day, week, month, year. For a very first version, 
business wants us to provide just the unique users per minute.   

- The data consists of (Log)-Frames of JSON data that are streamed into/from apache kafka. 
- Each frame has a timestamp property which is unix time, the name of the property is `ts`.
- Each frame has a user id property called `uid`. 
- You can assume that 99.9% of the frames arrive with a maximum latency of 5 seconds. 
- You want to display the results as soon as possible
- The results should be forwarded to a new kafka topic (again as JSON) choose a suitable structure. 
- For an advanced solution you should assume that you can **not** guarantee that events are always 
  strictly ordered.

## Sample data
For a quick start you can use the sample data provided at [http://tx.tamedia.ch.s3.amazonaws.com/challenge/data/stream.jsonl.gz](http://tx.tamedia.ch.s3.amazonaws.com/challenge/data/stream.jsonl.gz).It was generated using:
```shell script
./data-generator -c 1000000 -o stream.jsonl -r 1000 -n 100000
```

`cat stream.jsonl | jq .uid -r | gsort --parallel=4 | guniq | wc -l` yields `99993` unique ids.

You can input this file to your Kafka topic by doing something like:
```shell script
gzcat stream.gz | kafka-console-producer --broker-list localhost:9092 --topic mytopic
```  

You can also generate your own data by using the [data-generator tool](https://github.com/tamediadigital/hiring-challenges/tree/master/data-engineer-challenge/data-generator). It allows you to introduce random-ness if you have a more advanced solution and 
want to test it. You are required to install a Dlang compiler and D's package manager. Then 
execute `dub build` to build the binary. Also, binaries for OS X and Linux can be found in the bin 
directory.

## Suggested steps

#### Basic solution
1. Install Kafka
2. Create a topic
3. Use the Kafka producer from kafka itself to send our test data to your topic
4. Create a small app that reads this data from kafka and prints it to stdout
5. Find a suitable data structure for counting and implement a simple counting mechanism, output 
   the results to stdout

##### Advanced solution
6. Benchmark 
7. Output to a new Kafka Topic instead of stdout
8. Try to measure performance and optimize
9. Write about how you could scale
10. Only now think about the edge cases, options and other things

## Bonus questions / challenges:

- How can you scale it to improve throughput?
- You may want count things for different time frames but only do json parsing once.
- Explain how you would cope with failure if the app crashes mid day / mid year. 
- When creating e.g. per minute statistics, how do you handle frames that arrive late or frames 
  with a random timestamp (e.g. hit by a bitflip), describe a strategy?
- Make it accept data also from std-in (instead of Kafka) for rapid prototyping. (this might be 
  helpful to have for testing anyways)
- Measure also the performance impact / overhead of the json parser

## Hints
- Tap into other peoples know-how and code. 
- You should not use any big data framework, just your favorite fast programming language that has 
  a Kafka driver. The simplest version to achieve step 5 can be done with about 10 lines of code 
  (plus the boilerplate to read from Kafka). 
- If you found the cheatcode for level 5 (well done!) you should try to achieve level 10 ;)
- Check that your last commit compiles.
- Be smart and impress us. It does not matter if you impress us with nice clean code or with a 
  very clever hack to achieve the business goal in short time.

# Rules
We understand your time is precious and would not want you to spend more than **5 to 8 hours** on 
this over the span of **one week** max. The outcome should be runnable locally on a UNIX-flavored 
OS (MacOS, Linux).

## Functional requirements
- It should be possible to ingest historical data. e.g. from the last 2 years.
- Measure at least one performance metric (e.g. frames per second)

# What we expect
It is OK if the challenge is not completed. Try to **prioritize** it by what you think is more 
important. Tell us what motivated your technology choices, how you tackled the task, what you would 
do differently were you given more time, what you would differently a second time around, etc.

Together with your solution please provide a `README` file with the following:
- How to build and run the code
- A report, what did you do? What was the reasons you did it like that?
- Document your approach on how you decided **when** to output the data 
- Document the estimated error in counting

Here are some pointers for you of things we will be looking for:
- Ability to break down *business* requirements into simple prototype code
- Clean project setup and documentation
- Research and use of suitable data structure for a specific use case. explain which and why.
- Ability to write performant code to handle streaming data. measure and document _how_ fast your 
  solution is.
- Understanding how to benchmark and analyze performance bottle necks. what tools did you use?
- Awareness of the mechanisms and costs of serialization. Explain (and ideally prove!) why json is 
  an ideal format here or why not and then suggest a better solution.
- Scalability: _explain_ how you _would_ scale your approach

# Next steps

Send an email with a link to your repository solution.

We will review your solution, we strive to get back to you in **1 week**. Sometimes it might take 
more.
