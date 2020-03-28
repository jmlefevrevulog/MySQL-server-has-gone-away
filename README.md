# MySQL-server-has-gone-away

This repository solves issue where database connection inside of django overlives MySQL database connection timeout specified in `/etc/my.cnf` `wait_timeout = xxxx`. [See this issue](https://stackoverflow.com/questions/26958592/django-after-upgrade-mysql-server-has-gone-away)


## How to use:
1. pip install `mysql_server_has_gone_away`

2. Put this engine into Django `settings.py`:

```python
DATABASES = {
	'default': {
		'ENGINE': 'mysql_server_has_gone_away', 
		#'NAME': 'database-name',
		#'USER': 'database-user',
		#'PASSWORD': 'database-password',
		#'HOST': 'localhost',
	}
}
```
