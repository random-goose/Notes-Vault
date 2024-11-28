# PHP
### Features
- Server-Side Scripting
- Open source
- Cross-Platform
- Database Integration
- Dynamic Content
- Embedded into HTML
- Extensive Libraries
- High Performance
- Wide Connectivity
### Characteristics
- Simplicity
- Interpreted
- Scalable
- Loosely Typed
- Error Handling
- Session Management
### Installation Process
- Install Web Server
	- Install Apache, Nginx, or IIS
- Install PHP
	- Download from php.net
	- Configure it from the php.ini file
- Install Database
	- Install MySQL, MariaDB etc.
- Setup Environment
	- Add PHP to the system PATH
- Test
	- Create a `test.php` with the content `<?php phpinfo(); ?>`
	- Access it through a browser to verify the installation
### Applications
- Web Development
	- Dynamic Webpages and Apps
	- WordPress, Joomla
- E-Commerce
	- Magneto, OpenCart
- CMS
	- Content Management System
- Social Media
	- Facebook
- Data Management
- CLI Automation

## Scope in PHP
#### Global
Variables declared outside a function are global and can be accessed globally throughout the script
- Directly accessible outside any function
- To access inside a function; use the `global` keyword next to the variable name or import all the global variables using `$GLOBAL`

```php
$10 = 10;

function test() {
	global $x;
	echo $x;
}
test();

//or

function test(){
	echo $GLOBAL['x'];
}
test();
```

#### Local
Variables declared inside a function are local to that function and cannot be accused outside of it
- Local variables are created when the function is called and destroyed after execution

```php
function test() {
	$y = 69;
	echo $y;
}
test(); //output: 69
echo $y; //output: Error: Undefined variable $y
```

#### Static
Local variables that retain their value even after multiple function calls
- They are initialized after the function is called but are not destroyed after execution
- Used for preserving state between calls for counting or other purposes

```php
function test() {
	static $count = 0;
	$count++;
	echo $count . "\n";
}
test();// Outputs 1
test();// Outputs 2
test();// Outputs 3
```

