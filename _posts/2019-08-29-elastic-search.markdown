---
layout: post
title:  "Elastic search "
date:   2019-08-29 14:44:30 +0800
categories: 
---

$ELASTICSEARCH_HOME/config/elasticsearch.yml
{% highlight yaml %}
node.name: node-master
network.host: 0.0.0.0
http.port: 9200
{% endhighlight %}

$KIBANA_HOME/config/kibana.yml
{% highlight yaml %}
server.host: 0.0.0.0
{% endhighlight %}



{% highlight http %}
localhost:9200/_cat/indices
{% endhighlight %}

{% highlight http %}
localhost:9200/news?pretty
{% endhighlight %}

{% highlight http %}
localhost:9200/news/_search?pretty&size=30
{% endhighlight %}