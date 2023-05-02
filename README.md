<h1 align="center">
  <br>
  Easy PHP cURL Request
  <br>
</h1>

<h4 align="center">Free PHP Class to make Http Request using cURL</h4>

<p align="center">
  <a href="#how-to-use">How To Use</a> •
  <a href="#download">Download</a> •
  <a href="#license">License</a>
</p>


## How To Use

```bash
# Clone this repository
$ git clone https://github.com/hstanleycrow/EasyPHPcURLRequest/

# install libraries
$ composer update

# or install using composer
$ composer require hstanleycrow/easyphpcurlrequest
```

### Examples
```php

$url = "https://reqres.in/api/users";
$postData = array(
    'name' => 'John Doe',
    'job' => 'Web Developer'
);
$request = new CurlRequest($url);
$request->setPost(true);
$request->setPostData(json_encode($postData));
$request->setHttpHeader([
    'Content-Type: application/json'
]);
$request->execute();
if ($request->isSuccessful()) :
    $response = $request->getResult();
    $response_data = json_decode($response, true);
    var_dump($response_data);
else :
    echo "Error";
endif;

#example 2: get request
$url = 'https://jsonplaceholder.typicode.com/posts';
$request = new CurlRequest($url);
$request->setPost(false);
$request->setHttpHeader([
    'Content-Type: application/json'
]);
$request->execute();
if ($request->isSuccessful()) :
    $response = $request->getResult();
    $response_data = json_decode($response, true);
    var_dump($response_data);
else :
    echo "Error";
endif;

```


## Download

You can [download](https://github.com/hstanleycrow/EasyPHPcURLRequest/) the latest version here.

## PHP Versions
I have tested this class only in this PHP versions. So, if you have an older version and do not work, let me know.
| PHP Version |
| ------------- |
| PHP 8.0 | 
| PHP 8.1 |
| PHP 8.2 |

## Support

<a href="https://www.buymeacoffee.com/haroldcrow" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/purple_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>

## License

MIT

---

> [www.hablemosdeseo.net](https://www.hablemosdeseo.net) &nbsp;&middot;&nbsp;
> GitHub [@hstanleycrow](https://github.com/hstanleycrow) &nbsp;&middot;&nbsp;
> Twitter [@harold_crow](https://twitter.com/harold_crow)

