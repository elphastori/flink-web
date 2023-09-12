---
title: Apache Flink® — Stateful Computations over Data Streams
type: docs
hero: true
---
<!--
Licensed to the Apache Software Foundation (ASF) under one
or more contributor license agreements.  See the NOTICE file
distributed with this work for additional information
regarding copyright ownership.  The ASF licenses this file
to you under the Apache License, Version 2.0 (the
"License"); you may not use this file except in compliance
with the License.  You may obtain a copy of the License at

  http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an
"AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
KIND, either express or implied.  See the License for the
specific language governing permissions and limitations
under the License.
-->

<div class="panels code">
    <div class="wrapper">
        <div class="buttons">
            <div class="button">
                <a href="#">
                    <span>Java</span>
                </a>
            </div>
            <div class="button unselected">
                <a href="#">
                    <span>Scala</span>
                </a>
            </div>
            <div class="button unselected">
                <a href="#">
                    <span>SQL</span>
                </a>
            </div>
            <div class="button unselected">
                <a href="#">
                    <span>Python</span>
                </a>
            </div>
        </div>
    </div>
    <div class="wrapper">
        <div class="tabs">
            <div class="tab">
                <div class="tab-item selected">DataStream API</div>
                <div class="tab-item">Process Function API</div>
                <div class="tab-item">Table API</div>
            </div>
            <div class="tabcontent">
                <pre tabindex="0">
<code>DataStream<Tuple2<String, Integer>> dataStream = env
    .socketTextStream("localhost", 9999)
    .flatMap(new Splitter())
    .keyBy(value -> value.f0)
    .window(TumblingProcessingTimeWindows.of(Time.seconds(10)))
    .sum(1);</code>
                </pre>
            </div>
        </div>
    </div>
</div>

<div class="panels">
    <div class="title">Flink Capabilities</div>
    <div class="wrapper">
        <div class="panel">
            <div class="icon flink-compatibility-icon"></div>
            <div class="heading">Correctness guarantees</div>
            <div class="body">
                <p>Exactly-once state consistency</p>
                <p>Event-time processing</p>
                <p>Sophisticated late data handling</p>
            </div>
            <div class="button">
                <a href="/what-is-flink/flink-applications#building-blocks-for-streaming-applications">
                    <span>Learn more <i class="fa fa-chevron-right"></i></span>
                </a>
            </div>
        </div>
        <div class="panel">
            <div class="icon flink-layered-apis-icon"></div>
            <div class="heading">Layered APIs</div>
            <div class="body">
                <p>SQL on Stream & Batch Data</p>
                <p>DataStream API & DataSet API</p>
                <p>ProcessFunction (Time & State)</p>
            </div>
            <div class="button">
                <a href="/what-is-flink/flink-applications/#layered-apis">
                    <span>Learn more <i class="fa fa-chevron-right"></i></span>
                </a>
            </div>
        </div>
        <div class="panel">
            <div class="icon flink-operational-icon"></div>
            <div class="heading">Operational focus</div>
            <div class="body">
                <p>Flexible deployment</p>
                <p>High-availability setup</p>
                <p>Savepoints</p>
            </div>
            <div class="button">
                <a href="/what-is-flink/flink-operations/">
                    <span>Learn more <i class="fa fa-chevron-right"></i></span>
                </a>
            </div>
        </div>
        <div class="panel">
            <div class="icon flink-scalability-icon"></div>
            <div class="heading">Scalability</div>
            <div class="body">
                <p>Scale-out architecture</p>
                <p>Support for very large state</p>
                <p>Incremental checkpointing</p>
            </div>
            <div class="button">
                <a href="/what-is-flink/flink-architecture/#run-applications-at-any-scale">
                    <span>Learn more <i class="fa fa-chevron-right"></i></span>
                </a>
            </div>
        </div>
        <div class="panel">
            <div class="icon flink-performance-icon"></div>
            <div class="heading">Performance</div>
            <div class="body">
                <p>Low latency</p>
                <p>High throughput</p>
                <p>In-Memory computing</p>
            </div>
            <div class="button">
                <a href="/what-is-flink/flink-architecture/#leverage-in-memory-performance">
                    <span>Learn more <i class="fa fa-chevron-right"></i></span>
                </a>
            </div>
        </div>
    </div>
</div>

<div class="panels odd">
    <div class="title">Use Cases</div>
    <div class="wrapper">
        <div class="panel">
            <div class="icon flink-event-driven-icon"></div>
            <div class="heading">Event Driven Applications</div>
            <div class="body">
                <p>An event-driven application is a stateful application that ingest events from one or more event streams and reacts to incoming events by triggering computations, state updates, or external actions.</p>
            </div>
        </div>
        <div class="panel">
            <div class="icon flink-stream-batch-icon"></div>
            <div class="heading">Stream & Batch Analytics</div>
            <div class="body">
                <p>Analytical jobs extract information and insight from raw data. Traditionally, analytics are performed as batch queries or applications on bounded data sets of recorded events.</p>
            </div>
        </div>
        <div class="panel">
            <div class="icon flink-pipeline-etl-icon"></div>
            <div class="heading">Data Pipelines & ETL</div>
            <div class="body">
                <p>Extract-transform-load (ETL) is a common approach to convert and move data between storage systems.</p>
            </div>
        </div>
    </div>
    <div class="wrapper">
        <div class="button">
            <a href="/use-cases/">
                <span>Learn more about Flink use cases <i class="fa fa-chevron-right"></i></span>
            </a>
        </div>
    </div>
</div>

{{< recent_posts >}}
