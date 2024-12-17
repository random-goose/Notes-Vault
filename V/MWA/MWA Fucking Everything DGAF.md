# Unit I
### Website: Uses and Purpose
A website is a collection of related web pages hosted on the internet, accessible via a unique domain name.
It serves as a platform for sharing information, communication, commerce, and interaction.

Need:
- Accessibility - Provides a globally available 24/7 access to information and services
- Cost-Effectiveness - Reduces the need for physical infrastructure
- Convenience - Streamlines communication and transactions for users
- Information Sharing - provide a global platform to share and retrieve information
- Business Growth - in the present economy, having an online presence is essential for business

Purpose:
- Information Sharing - Disseminates knowledge, updates, and guidance
- Business Growth - Facilitates marketing, customer engagement, and sales
- Brand Presence - enhances visibility, and credibility of organizations or individuals 
- Interaction - Enables user engagement through tools like forms, chat or e-commerce
- Entertainment - To dtream or download music, video, or images


### Static and Dynamic Websites
#### Static
They consist of fixed content delivered to users exactly the way it is stored. The pages are pre-rendered and do not change unless manually updates by a developer.

Characteristics:
- Built using basic web technologies like HTML, CSS, and optional JavaScript for minor interactivity
- Each page is a separate file stored on the server, and there is no database involved.
- Best suited for smaller websites such as personal portfolios, informational sites, or company profiles with minimal updates
Advantages
- Fast Loading - because the pages are pre-rendered and there is no reliance on databases or backend, pages load quickly
- Cost Effective - Simple to develop, host, and maintain
- High Security - without any backend interaction, they are inherently secure
Disadvantages
- Static Content - content remains the same unless manually updated
- Scalability Issues - Not ideal for websites that require frequent updates or user interaction
- Limited functionality - Cannot handle complex tasks

#### Dynamic
generate content in real-time base don user interactions, external data, or backend logic. The content changes dynamically, making these websites more interactive and versatile

Characteristics
- Built using server-side scripting using languages and frameworks like python - Django, JavaScript - Node, or PHP
- Typically connected to a database to store and retrieve information
- Used for complex applications like e-commerce platforms, social media sites, or blogs with frequent updates and interactivity are essential
Advantages
- Interactive Content - Provides a personalized experience for users by tailoring content based on their actions or preferences
- Easy Updates - using Content Management Systems (CMS) like WordPress allow non-technical suers to update content effortlessly
- Advances Features - Supports functionality like authentication, data processing, and e-commerce
Disadvantages
- Higher Deployment Costs
- Slower Loading times
	- Database Queries
	- Server-side rendering
- Increased Security Risks - More Vulnerable

### HTML
Hyper Text Markup Language is a standard markup language used to create and design web pages
It structures content on the web, defining elements like text, images, links, and multimedia
- Uses predefined tags
- Focuses on visual presentation and user interaction
- Supports links to navigate across web pages
- Creating the structures of websites
- Designing forms, tables, and multimedia content

```HTML
<html>
	<head>
		<title>MWA Sem Prep Bruh Ohio Moment frfr</title>
	</head>
	
	<body>
		<h1>I am the skibidi</h1>
		<h2>You are the Rizzler</h2>
		<ul>
			<li>List Item Lol</li>
			<li>Another One</li>
		</ul>
	</body>
<html>
```

### XML
extensible Markup Language is a markup language designed to store and transport data in a structure and readable format
Focuses on data storage and exchange rather than presentation
- Customizable tags - allows users to create own tags
- Hierarchical Structure - trees
- Platform-independent
- Data exchange between applications
- Configuration files

```XML
<? xml version = "1.0" encoding = "utf-8"?>
<bookstore>
	<book>
		<title>Ohio Documentary</title>
		<author>Hawk Tuah</author>
		<price currency="DOGE">1000</price>
	</book>
	<book>
		<title>Rizzler Guide</title>
		<author>UwU</author>
		<price currency="INR">42069</price>
	</book>
```

### JSON
JavaScript Object Notation is a lightweight data-interchange format that is easy for humans to read and write and for machines to parse and generate
Is primarily used for transmitting data between a server and a web app
- Simplicity - key:value
- Lightweight
- Language-Independent
- APIs for data exchange
- Storing configuration and state info

```JSON
{
	"books" : {
		{
			"title": "Rizzler Guide",
			"author": "uwu",
			"price": [
				"amount" : 69420,
				"currency" : "INR"
			]
		},
		{
			"title": "Ohio Documentary",
			"author": "Hawh Tuah",
			"price": [
				"amount" : 42069,
				"currency" : "DOGE"
			]
		},
	}
}
```

| Feature         | HTML                  | XML                     | JSON                     |
| --------------- | --------------------- | ----------------------- | ------------------------ |
| **Purpose**     | Web content structure | Data storage & exchange | Data transmission        |
| **Format**      | Predefined tags       | Customizable tags       | Key-value pairs          |
| **Readability** | Human-readable        | Human-readable          | Highly human-readable    |
| **Usage**       | Website design        | Inter-application data  | APIs and web development |

## URL
Uniform Resource Locator is a part of the World Wide Web standard proposed by Tim Berners-Lee, and is a string which acts like an address and is used to locate different resources like web pages, photos, or videos.

### Structure
https://www.github.io:8080/random-goose?query=where+is+ohio#results 
https:// → Protocol
www.github.io → Domain Name
:8080 → Port Number
/random-goose → Path
?search→ Query
/# results → Fragment

Absolute URL → www.rangomgoose.com/profile/images/progile_picture.jph
Relative URL → images/profile_picture.jpg

Importance of URLs:
- Resource Identification
- Navigation
  Data Transfer
  Linking Content

## Web Programming Languages
- HTML
- CSS
- JavaScript
- Python
- PHP
- Ruby
- C#
- TypeScript
- SQL
- Kotlin - Android
- Swift - Apple


# Unit III
## Features of JavaScript
1. Client Side Scripting
3. Dynamically Typed
4. Event - Driven Programming
5. Lightweight and Fast
6. Object-Oriented
7. Asynchronous
8. DOM Manipulation
ECD LOAD
Event Driven
Client Side Scripting
Dynamically Typed
Lightweight
Object-Oriented
Asynchronous
DOM
# Unit IV

### GET
```javascript
fetch('http://api.skibidi.com/users?69')
	  .then (response => response.json())
	  .then (data => consloe.log(data));
```

### POST
```javascript
fetch('http://api.skibidi.com/users', {
	method: 'POST',
	headers: {
		'Content-Type' : 'application/json'
	},
	body: JSON.stringify ({
		name: 'Rizzler',
		email: 'rizzler@ohio.bruh'
	})
})
	.then(respone => responce.JSON())
	.then(data => console.log(data));
```

### PUT
```js
fetch('http://api.skibidi.com/users', {
	method: 'PUT',
	headers: {
		'Content-Type' : 'application/json'
	},
	body: JSON.stringify ({
		name: 'Rizzler',
		email: 'rizzler@ohio.bruh'
	})
})
	.then(respone => responce.JSON())
	.then(data => console.log(data));
```

### DELETE
```js
fetch('http://api.skibidi.com', {
	method: 'DELETE'
})
.then(response => console.log("Deleted"));
```

## PHP Operators
Arithmetic:
- +
- -
- *
- /
- %
Assignment:
- =
- +=
- -=
- /=
- * =
- %=
Comparison:
- <
- >
- ==
- ===
- !=
- >=
- <=
- !==
Increment / Decrement:
- ++
- /- /-
Logical:
- &&
- ||
- ^
- !

## HTML Form
```html
<html>
	<body>
		<form action = 'Welcome.PHP' method = "POST">
			Name : <input type="text" name = "name"> <br>
			Email : <input type="text" name = "email">
			<input type="submit" value="Submit">
		</form>
	</body>
</html>
```
```PHP
<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
	$name = $_POST['name'];
	$email = $_POST['email'];
	echo "welcome: " . htmlspecialchars($name) . "!<br>";
	echo "your email is: " . htmlspecialchars($email) . ".<br>";
	
}
```

## Cookie 🍪

```php
setcookie(name, value, epire, path, domain, security, httponly);
```

```php
<?php
setcookie("username", "rizzler", time() + 3600, "/");
echo "cookie 'username' is set! <br>"
?>
```

```php
<?php
if(isset($_COOKIE["username"])) {
	echo "welcome, " . htmlspecialchars($_COOKIE['username']) . ".<br>";
} else {
	echo "Cookie not set";
}
```

## Session

```php
<?php
session_start();

$_SESSION["username"] = 'Rizzler';
$_SESSION["email"] = 'hawk@tuah.rizz';

echo "session set"

if (isset($_SESSION["username"])) {
	echo "Welcome " . $_SESSION["username"] . ". <br>"
	echo "You email is " . $_SESSION["email"] . ". <br>"	
} else {
	echo "No session data found"
}

session_unset();

session_destroy();

if (isset($_SESSION["username"])) {
	echo "Welcome " . $_SESSION["username"] . ". <br>"
	echo "You email is " . $_SESSION["email"] . ". <br>"	
} else {
	echo "No session data found"
}

echo "Session destroyeyd."
?>

```

# Unit V
## JDBC
- Driver Manager
- Driver
- Connection
- Statement
- Result Set
- SQL Exception