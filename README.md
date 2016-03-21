# Bigdesk

Live charts and statistics for Elasticsearch 2.x cluster.

## 03-21-2016
- Support for Elasticsearch 2.x

## Installation Instructions

Install Elasticsearch then navigate to `<ES_HOME>` and execute the following command on command line:

    $ ./bin/plugin -install hlstudio/bigdesk

## How to use Bigdesk

Once you open Bigdesk in your web browser, you need to **point it to the Elasticsearch node REST endpoint**.
For example if you run Elasticsearch locally the REST endpoint would be `http://localhost:9200/` by default.
You simply specify any endpoint URL in the text field on top of the Bigdesk screen (or via URL parameter, see below).

If you are using Bigdesk **1.0.0** (ie. you want to connect Bigdesk to elasticsearch 0.17.x - 0.18.x) then you need
to fill into two different text fields. First you specify **hostname** of the Elasticsearch node into the first
text field and its **port** number into the second text field (but in some situations this can be limiting,
for example if you run Elasticsearch behind firewall).

Then you hit **Connect** button (it is called **GO!** button in Bigdesk 1.0.0) and that's it.

Now you should see cluster name and list of its nodes. You can switch between nodes in the cluster, new nodes are added
and old nodes are removed automatically on the fly.

You can change the Bigdesk **refresh interval** and **amount of data** that is displayed by charts.

### URL parameters

If you are using **Bigdesk 1.0.0** you can immediately connect to a particular host, add the
`host`, `port`, and `go` parameters to the query string:

	index.html?host=search.example.com&port=9200&go

If you are using **Bigdesk 2.x** you can use any of the following URL parameters to immediately connect to
a particular host or set history or refresh interval:

- `endpoint` = URL of ES node REST endpoint (you might want to use URL encoded value). Defaults to `http://localhost:9200`.
- `refresh` = refresh interval in milliseconds. Defaults to `2000` (2 sec).
- `history` = number of milliseconds to keep in history. Defaults to `300000` (5 min).
- `connect` = if set to `true` Bigdesk will try to connect immediately to the endpoint. Defaults to `false`.

Example connecting to `http://127.0.0.1:9201` with 3 sec refresh interval:

	index.html?endpoint=http%3A%2F%2F127.0.0.1%3A9201&refresh=3000&connect=true

## Screenshots

![Bigdesk ES2.x](https://github.com/hlstudio/bigdesk/raw/master/bigdesk-es2.png)


## Supported Web Browsers

Bigdesk should work in all modern web browsers as long as they support SVG. It has been tested in Safari, Firefox and Chrome.

## Credits

Lukas Vlcek and [contributors](https://github.com/lukas-vlcek/bigdesk/contributors).
Modified by hlstudio.
