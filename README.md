# OneClick Login for Adminer
Display a list of predefined database servers to login with just one click. V2
Our use case is base on Kubernetes or docker. And bypass the setting  via environment. We recommand this can be used on stage/beta environment only. 
Don't use this in production enviroment unless the access is restricted


## Usage
Create a environment variable `ADMINER_SERVERS` that can be access by PHP. 
`ADMINER_SERVERS` define your database details with the following structure
```
scheme://username:pass@host:port/table
```
If you have multiple server to define, please use `,` to concat all of the settings. The following is the example. 
```
ADMINER_SERVERS=mysql://root:root@127.0.0.1:3306/table1,mysql://root:root@127.0.0.1:3306/table2,mysql://root:root@mariadb:3306/table3
```

Instantiate OnClick Login V2 according to adminer instructions from [adminer](https://www.adminer.org/plugins/#use)
```
new OneClickLoginV2();
```