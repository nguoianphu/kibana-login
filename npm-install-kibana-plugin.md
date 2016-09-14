# Kibana Plugin Yeoman Generator

This project is a Yeoman generator for bootstrapping a Kibana Plugin. It creates a basic hello world Kibana plugin with all the elements in place so you can easily get started with creating your first Kibana plugin.

## Getting Started

First you need to install Yeoman

```
npm install -g yo
```

Then you need to install the Kibana Plugin generator

```
npm install -g generator-kibana-plugin
```

Then generate your new plugin

```
mkdir my-login
cd my-login
yo kibana-plugin
npm start
```

Assuming you've setup a [Kibana development enviroment](https://github.com/elastic/kibana/blob/master/CONTRIBUTING.md#development-environment-setup) at the same level as your plugin directory (and named it `kibana`). Then run the following command inside your plugin directory.

```
cd ..
git clone https://github.com/elastic/kibana.git kibana
cd kibana
git checkout 4.6
nvm install "$(cat .node-version)"
npm install
```

Start Elasticsearch

```
npm run elasticsearch
npm run makelogs
```

or 

```
mkdir ../elasticsearch
cd ../elasticsearch
export ES_HEAP_SIZE=256m
export ES_JAVA_OPTS="-Xms256m -Xmx256m"
curl -L -O https://download.elastic.co/elasticsearch/release/org/elasticsearch/distribution/tar/elasticsearch/2.4.0/elasticsearch-2.4.0.tar.gz
tar -xvf elasticsearch-2.4.0.tar.gz
cd elasticsearch-2.4.0/bin
./elasticsearch
```



Start Kibana in dev mode.

```
bin/kibana --dev
```

Visit [http://localhost:5601](http://localhost:5601)

## options

If you start the generator with the `--minimal` flag, it will not generate any sample code only
the bare folder structure.

If you start the generator with the `--advanced` flag, you can choose what sample
components it should generate for you.
