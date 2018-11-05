# OutOfOffice

## HOW TO SET UP THE OUT OF OFFICE WEB PAGE TAKEOVER

## STANDARD WEBSITE / FTP

1. If you have access to the index.html page, you can copy and paste the following CSS and JavaScript links in between the `<head>` and `</head>` tags:
```
<link rel="stylesheet" type="text/css" href="https://www.thisisnow.com/wep/OutOfOffice.css">
<script type="text/javascript" src="https://www.thisisnow.com/wep/OutOfOffice.js"></script>
```
You should immediately be able to see the glitchy alert message when reloading your website.

To disable the effect these links add to your website, simply remove them from the index file mentioned above.


## WORDPRESS

The following options to update your WordPress website will most likely require an admin account.

###### OPTION 1

The fastest implementation of the Out Of Office on a WordPress website does not require any plugins:

1. Open the **WP admin dashboard** for your website
2. Navigate to **Appearance > Editor**
3. Select **functions.php** from Theme Files
4. Insert the following code at the end of the document, before the **?>**
```
// Out Of Office
function out_of_office() {
	echo '<link rel="stylesheet" type="text/css" href="https://www.thisisnow.com/wep/OutOfOffice.css">';
	echo '<script type="text/javascript" src="https://www.thisisnow.com/wep/OutOfOffice.js"></script>';
}
add_action( 'admin_head', 'out_of_office' );
add_action( 'wp_head', 'out_of_office' );
```
###### OPTION 2

If you prefer to avoid touching any code, an alternative is possible using a very simple plugin:

1. Open the **WP admin dashboard** for your website
2. Navigate to **Plugins > Add New**
3. Search for the plugin called **Head, Footer and Post Injections** by _Stefano Lisa_
4. Click the **Install Now** button on the plugin to install it
5. Click the **Activate** button once the installation is complete
6. Navigate to **Settings > Header and Footer**
7. In the **<HEAD> PAGE SECTION INJECTION** box (either _ON EVERY PAGE_ or _ONLY ON THE HOME PAGE_ - whatever is your preference) paste the following CSS and JavaScript links:
```
<link rel="stylesheet" type="text/css" href="https://www.thisisnow.com/wep/OutOfOffice.css">
<script type="text/javascript" src="https://www.thisisnow.com/wep/OutOfOffice.js"></script>
```

## SQUARESPACE

If you run your website through **SquareSpace**, the steps are simple:

1. Open the **SquareSpace admin dashboard** for your website
2. Navigate to **Pages**
3. Click the **Cog / Settings** button for your home page
4. Navigate to **Advanced**
5. Paste the following code into **Page Header Code Injection** and click **save**:
```
<link rel="stylesheet" type="text/css" href="https://www.thisisnow.com/wep/OutOfOffice.css">
<script type="text/javascript" src="https://www.thisisnow.com/wep/OutOfOffice.js"></script>
```

## ADVANCED / CUSTOM IMPLEMENTATION

If you have an advanced technical knowledge and would prefer to implement the CSS and JavaScript files manually and/or you prefer not to link external files into your website, you may download the [source files from here](https://www.thisisnow.com/wep/OutOfOffice.zip)

_Developed at [**Now**](https://www.thisisnow.com/)._

