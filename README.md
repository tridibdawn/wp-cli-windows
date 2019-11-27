# WP CLI Windows Installation

__1. Install Composer__

Download and install the [Composer](https://getcomposer.org/doc/00-intro.md#installation-windows) . It will install the latest Composer version and set up your PATH so that you can just call composer from any directory in your command line.

To verify composer installed successfully, open your command prompt and type,

```composer -v```

__2. Install PHP__

You probably have XAMPP already installed in your system that already installed the PHP environment. To verify PHP exist in your system, try checking its version. open your command prompt and type, Remember your apache service needs to be started for this process to check.

```php -v```

__3. Begin install WP CLI__

Once above set up are completed, download phar file. Let’s say you want to install wp-cli in your F: drive, you just go and place this phar file in a logical path F:\wp-cli\wp-cli.phar . Now create a new batch file wp.bat in the same directory, this will act as an alias for the phar file. Inside wp.bat file paste the following contents and save.

```
@ECHO OFF
php "%~dp0wp-cli.phar" %*
```

__4. Set environment variable__

Go to __System’s Properties__ -> click __Advanced System Properties__ -> select the tab labeled __Advanced__. Click __Environment Variables__, under the __System Variables__ section scroll down to the variable named __Path__ and add __;C:\wp-cli__
