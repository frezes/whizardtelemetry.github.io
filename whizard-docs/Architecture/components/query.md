# Query

Query是 Thanos 的原生组件之一，它提供了强大的查询功能，以实现跨多个数据源的分布式查询。下面是 Query 的主要功能：

1. **全局查询视图**： Query可以将多个Prometheus实例和对象存储中的数据合并为一个全局查询视图。它提供了一个统一的查询接口，使您能够跨多个数据源执行查询操作，而无需直接与每个数据源交互。
    
2. **查询数据聚合**： Query支持在查询时对数据进行聚合操作，如求和、平均值、最大值等。您可以根据需要对时间序列数据进行聚合，从而得到更高级别的统计结果。
    
3. **查询优化**： Query具有智能的查询优化功能，它可以利用Thanos的元数据存储（如Store）来识别并跳过不包含所需数据的数据源。这样可以提高查询性能并减少数据传输的开销。
    
4. **查询时间范围选择**：您可以在 Query中指定查询的时间范围，以获取特定时间段内的数据。这使您可以根据需要收集有关特定时间窗口的指标数据。
    
5. **支持Prometheus查询语言**： Query支持Prometheus查询语言（PromQL），这是一种功能强大的查询语言，用于检索和分析时间序列数据。您可以使用PromQL查询语句来执行各种复杂的查询和聚合操作。
    

通过 Query，您可以跨多个数据源执行复杂的查询操作，获取全局视图，并利用Thanos的分布式能力和查询优化功能，提高查询性能和效率。