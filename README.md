# To actually run OpenTSDB, you'll need to meet the following:
1. A Linux system 16.04 LTS
    - 3GB RAM
    - 3 processors 2.4 GHZ
    - 64 bits
    - 40 GB SSD
1. Java Runtime Environment 1.8 oracle [Instalation Tutorial](https://www.digitalocean.com/community/tutorials/how-to-install-java-with-apt-get-on-ubuntu-16-04)
    - `JAVA_HOME must be stablished`.
1. HBase 1.2.6 [Instalation](http://hbase.apache.org/0.94/book/quickstart.html)
1. GnuPlot 4.2 or later `sudo apt-get install gnuplot`
1. AUTORECONF `sudo apt-get install dh-autoreconf`
1. Download OpenTSDB [Link](https://github.com/OpenTSDB/opentsdb/releases)
1. Install OpenTSDB `sudo dpkg -i opentsdb*.deb`
1. Verify settings in `/etc/opentsdb/* (nano /etc/opentsdb/*)`
1. Prepare enviroment
    - `sudo env COMPRESSION=NONE HBASE_HOME=/hbase/path/hbase-1.2.6 /usr/share/opentsdb/tools/create_table.sh`
1. Start opentsdb
    - `sudo service opentsdb start`
    - `sudo service opentsdb stop`
    - `sudo service opentsdb status`
    - [issue solution](https://github.com/OpenTSDB/opentsdb/issues/480)
1. HBASE is running in `http://localhost:16010/master-status`
1. OpenTSDB is running in `http://localhost:4242/`

References [opentsdb instalation](http://www.codeando.com/articles--artiacuteculos/installing-opentsdb-on-ubuntu-1604-lts)

# Modeling Data
The most important thing before start writing data is to think about the [`Naming Schema`](http://opentsdb.net/docs/build/html/user_guide/writing.html).

More [information](http://opentsdb.net/docs/build/html/user_guide/query/timeseries.html).
Even [more](https://www.digitalocean.com/community/tutorials/how-to-install-java-with-apt-get-on-ubuntu-16-04)

How to write data [click](http://www.erol.si/2014/06/opentsdb-the-perfect-database-for-your-internet-of-things-projects/)

Configuration [file](https://gist.github.com/kylebrandt/8c09c87fd3147fb51bc3)
