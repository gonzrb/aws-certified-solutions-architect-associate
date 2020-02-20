1- What is Straming Data?

- Straming Data is data that is generated continously bu thousands of data sources, which typically send in the data records simultaneously, and in small sizes (order of Kilobytes)
    - Purchases from online stores (think amazon.com)
    - Stock Prices
    - Game data (as the gamer plays)
    - Social network data
    - Geospatial data (think of uber.com)
    - iOT sensor data

2- What is Kinesis?

- Amazon Kinesis is a platform on AWS to send your streaming data to. Kinesis makes it easy to load an analyze straming data, and also providing the ability for you to build your own custom applciations for your business needs.

3- Kinesis types
    - Kinesis Streams: 
        - Kinesis Streams Consist of Shards: 7hours - 14 days persistances.
            - 5 transactions per second for reads, up to a maximum total data read rate of 2 MB per second and up to 1000 records per second for writes, up to a maximum total data write rate of 1MB per second (including partition keys).
            - The data capacity of your stream is a function fo the number of shards that you specify for the stream. The total capacity of the stream is the sum of the capacities of its shards.
    - Kinesis Firehose: 
        - Realtime processing, external storage.
    - Kinesis Analytics: Analizes data inside both.
