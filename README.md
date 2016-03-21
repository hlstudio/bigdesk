# Bigdesk

Live charts and statistics for Elasticsearch 2.x cluster.

## 2016-03-21
- Support for Elasticsearch 2.x

## Installation Instructions

Install Elasticsearch then navigate to `<ES_HOME>` and execute the following command on command line:

    $ ./bin/plugin -install hlstudio/bigdesk

## How to use Bigdesk

Open your web browser to access `http://127.0.0.1:9200/_plugin/bigdesk` by default.

Now you should see cluster name and list of its nodes. You can switch between nodes in the cluster, new nodes are added
and old nodes are removed automatically on the fly.

You can change the Bigdesk **refresh interval** and **amount of data** that is displayed by charts.


## Screenshots

![Bigdesk ES2.x](https://github.com/hlstudio/bigdesk/raw/master/bigdesk_es2.png)


## Supported Web Browsers

Bigdesk should work in all modern web browsers as long as they support SVG. It has been tested in Safari, Firefox and Chrome.

## Credits

Lukas Vlcek and [contributors](https://github.com/lukas-vlcek/bigdesk/contributors).

Modified by hlstudio.
