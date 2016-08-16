# ci_log4php
Intergrate log4php(2.3.0) with Codeigniter(+2.0). Add log data in your database or write code in file. 

1.) You need to create table in your database.

	CREATE TABLE log4php_log (
    timestamp DATETIME,
    logger VARCHAR(256),
    level VARCHAR(32),
    message VARCHAR(4000),
    thread INTEGER,
    file VARCHAR(255),
    line VARCHAR(10)
);

2.) Add log4php folder in your application/third_party/.

	application/third_party/log4php
	
3.) Add My_log.php file in application/libraries/.

	application/libraries/My_log.php
	
4.) Add $config['log_threshold'] = 4; in your project config.php file.

	application/config/config.php
	
5.) Add log4php.properties file in application/config/.

	application/config/log4php.properties
	add database details in this file.
6.) Add log4php.properties file in application/helpers/.

	application/helpers/log4php_helper.php
	
7.) Access code using below syntax.
 
	$this->load->helper('log4php');
	log_error('my_error');
	log_info('my_error');
