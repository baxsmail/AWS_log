## Plateform : Amazon Linux

### set up nginx environment
* install gcc compiler
```
yum -y install gcc
yum -y install gcc-c++
yum -y install make automake
```
* add user www
```
useradd KanZheQiMing
```
* install dependencies 
```
yum -y install pcre-devel openssl openssl-devel
sudo yum install 'perl(ExtUtils::Embed)' 'rubygem(minitest)'
or
yum -y install perl-devel perl-ExtUtils-Embed
```
* download and install nginx
```
./configure --user=www --group=www --with-http_stub_status_module --with-http_ssl_module --with-http_perl_module
make && make install
```

### set up mysql 
* pull from repository
```
yum install mysql
```

* limitation [issue](https://dev.mysql.com/doc/refman/5.6/en/ha-vm-aws-instance.html "Title")
