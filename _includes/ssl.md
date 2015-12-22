# SSL Certificate API

## List Certificates

Returns a list of all certificates on the specified account

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/ssl.json</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`certificates` | An array of certificates for the given user |

### Code Samples

<ul class="nav nav-tabs" id="myTab106">
  <li class="active"><a href="#ruby106" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python106" data-toggle='tab'>Python</a></li>
  <li><a href="#perl106" data-toggle='tab'>Perl</a></li>
  <li><a href="#php106" data-toggle='tab'>PHP</a></li>
  <li><a href="#node106" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp106" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#java106" data-toggle='tab'>Java</a></li>
  <li><a href="#response106" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby106">
    <pre>
api.get('/ssl.json')</pre>
  </div>
  <div class="tab-pane" id="python106">
    <pre>
api.get('/ssl.json')</pre>
  </div>
  <div class="tab-pane" id="perl106">
    <pre>
$api->get("/ssl.json");
</pre>
  </div>
  <div class="tab-pane" id="php106">
    <pre>
$api->get('/ssl.json');</pre>
  </div>
  <div class="tab-pane" id="node106">
  <pre>
api.get('/ssl.json', callback)
function callback(err, response) {
  if (err) return console.log(err)
  console.log(response)
}</pre>
  </div>
  <div class="tab-pane" id="csharp106">
  <pre>
api.Get("/ssl.json");
</pre>
  </div>
  <div class="tab-pane" id="java106">
  <pre>MaxCDNObject response = api.get("/ssl.json");
Console.log(response.error ? "Error " + response.getErrorMessage()  : response.code);</pre>
</div>
<div class="tab-pane" id="response106">
    <pre>
{
    "code": 200,
    "data": {
        "current_page_size": 1,
        "page": 1,
        "page_size": "50",
        "pages": 1,
        "total": 1,
        "certificates": [
            {
                "id": "1234",
                "company_id": "42",
                "domain": "*.example.com",
                "zone_count": "5",
                "date_updated": "2013-05-15 17:33:09",
                "date_expiration": "2015-11-15",
                "ssl_cabundle": "",
                "globalsign": "0",
                "wilcard": "1",
                "ssl_crt": "-----BEGIN CERTIFICATE-----\n...-----END CERTIFICATE-----",
                "name": "auto_*.example.com_2015-11-15_2013-05-15:173309"
            }
        ]
    }
}</pre>
  </div>
</div>

## Create Certificate

Creates a new SSL Certificate on the specified account

<div class="heading">
<div class="url POST"><span class="http_method">POST</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/ssl.json</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`ssl_crt` | - | <span class="label important">required</span><br />length: text; | Certificate  |
`ssl_key` | - | <span class="label important">required</span><br />length: text | Certificate Private Key |
`ssl_cabundle` | - | length: text | Certificate Authority Intermediate Bundle |
`name` | auto_{domain}_{expiration}_{update} | length: 1-255 | Use descriptive name |


### Response Parameters

Parameter | Description |
--- | --- | ---
`ssl` | The information about the certificate (see List Certificates response)|


### Code Samples

<ul class="nav nav-tabs" id="myTab107">
  <li class="active"><a href="#ruby107" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python107" data-toggle='tab'>Python</a></li>
  <li><a href="#perl107" data-toggle='tab'>Perl</a></li>
  <li><a href="#php107" data-toggle='tab'>PHP</a></li>
  <li><a href="#node107" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp107" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#java107" data-toggle='tab'>Java</a></li>
  <li><a href="#response107" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby107">
    <pre>
params={"ssl_crt"=>"-----BEGIN CERTIFICATE-----\n{ you certificate info }\n-----END CERTIFICATE-----","ssl_key"=>"-----BEGIN RSA PRIVATE KEY-----\n{ your private key info}\n-----END RSA PRIVATE KEY-----","ssl_cabundle"=>"-----BEGIN CERTIFICATE.....", "name"=>"Our *.example.com wildcard"}
api.post('/ssl.json',params )</pre>
  </div>
  <div class="tab-pane" id="python107">
    <pre>
params = array("ssl_crt": "-----BEGIN CERTIFICATE-----\n{ you certificate info }\n-----END CERTIFICATE-----","ssl_key": "-----BEGIN RSA PRIVATE KEY-----\n{ your private key info}\n-----END RSA PRIVATE KEY-----","ssl_cabundle": "-----BEGIN CERTIFICATE.....", "name": "Our *.example.com wildcard");
api.post('/ssl.json',data=params )</pre>
  </div>
  <div class="tab-pane" id="perl107">
  <pre>
my @params = {ssl_crt => '-----BEGIN CERTIFICATE-----\n{ you certificate info }\n-----END CERTIFICATE-----', ssl_key => '-----BEGIN RSA PRIVATE KEY-----\n{ your private key info}\n-----END RSA PRIVATE KEY-----","ssl_cabundle"=>"-----BEGIN CERTIFICATE.....", "name"=>"Our .example.com wildcard');
$api->post("/ssl.json", @params );
  </pre>
  </div>
  <div class="tab-pane" id="php107">
    <pre>
$params = array("ssl_crt"=>"-----BEGIN CERTIFICATE-----\n{ you certificate info }\n-----END CERTIFICATE-----","ssl_key"=>"-----BEGIN RSA PRIVATE KEY-----\n{ your private key info}\n-----END RSA PRIVATE KEY-----","ssl_cabundle"=>"-----BEGIN CERTIFICATE.....", "name"=>"Our *.example.com wildcard");
$api->post('/ssl.json',$params );</pre>
  </div>
  <div class="tab-pane" id="node107">
  <pre>
api.post('/ssl.json', { ssl_crt:"-----BEGIN CERTIFICATE-----\n{ you certificate info }\n-----END CERTIFICATE-----",ssl_key:"-----BEGIN RSA PRIVATE KEY-----\n{ your private key info}\n-----END RSA PRIVATE KEY-----",ssl_cabundle:"-----BEGIN CERTIFICATE.....",name:"Our *.example.com wildcard" }, callback)
function callback(err, response) {
  if (err) return console.log(err)
  console.log(response)
}</pre>
  </div>
  <div class="tab-pane" id="csharp107">
  <pre>
var cert = "";
var key = "";
Console.Write("Zone id: \n");
int zoneId = Convert.ToInt32(Console.ReadLine());
Console.Write("Zone type: \n");
string type = Console.ReadLine();
using (StreamReader sr = new StreamReader("cert.txt"))
{
cert = sr.ReadToEnd();               
}
using (StreamReader sr = new StreamReader("key.txt"))
{
key = sr.ReadToEnd();
}
var dat = "";
cert = "-----BEGIN CERTIFICATE-----\n" + cert + "\n-----END CERTIFICATE-----\n";
key = "-----BEGIN RSA PRIVATE KEY-----\n" + key + "\n-----END RSA PRIVATE KEY-----\n";

api.Post("/ssl.json", dat="ssl_crt=" + cert + "&ssl_key=" + key);
</pre>
  </div>
  <div class="tab-pane" id="java107">
  <pre>String ssl_crt = "-----BEGIN CERTIFICATE-----\n{ ... your certificate ... }\n-----END CERTIFICATE-----\n";
String ssl_key = "-----BEGIN RSA PRIVATE KEY-----\n{ ... your key ... }\n-----END RSA PRIVATE KEY-----";
String name = "Our *.example.com wildcard";
MaxCDNRequest data = MaxCDN.newRequest("ssl_crt", "ssl_crt").append("ssl_key", "ssl_key").append("name", "name");
MaxCDNObject response = api.post("/ssl.json", data);
Console.log(response.error ? "Error " + response.getErrorMessage()  : response.code);</pre>
</div>
<div class="tab-pane" id="response107">
    <pre>
{
    "code": 200,
    "data": {
        "current_page_size": 1,
        "page": 1,
        "page_size": "50",
        "pages": 1,
        "total": 1,
        "ssl": 
            {
                "id": "1234",
                "company_id": "42",
                "domain": "*.example.com",
                "zone_count": "5",
                "date_updated": "2013-05-15 17:33:09",
                "date_expiration": "2015-11-15",
                "ssl_cabundle": "",
                "globalsign": "0",
                "wilcard": "1",
                "ssl_crt": "-----BEGIN CERTIFICATE-----\n...-----END CERTIFICATE-----",
                "name": "Our *.example.com wildcard"
            }
    }
}</pre>
  </div>
</div>

## Get SSL Certificate

Gets a specific SSL certificate by the {ssl_id} parameter

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/ssl.json/{ssl_id}</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`ssl` | The information about the certificate (see List Certificates response)|


### Code Samples

<ul class="nav nav-tabs" id="myTab108">
  <li class="active"><a href="#ruby108" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python108" data-toggle='tab'>Python</a></li>
  <li><a href="#perl108" data-toggle='tab'>Perl</a></li>
  <li><a href="#php108" data-toggle='tab'>PHP</a></li>
  <li><a href="#node108" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp108" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#java108" data-toggle='tab'>Java</a></li>
  <li><a href="#response108" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby108">
    <pre>
id = '1234'
api.get('/ssl.json/'+id)</pre>
  </div>
  <div class="tab-pane" id="python108">
    <pre>
id = '1234'
api.get('/ssl.json/'+id)</pre>
  </div>
  <div class="tab-pane" id="perl108">
    <pre>
my $id = 1234;
$api->get("/ssl.json/" . $id);
</pre>
  </div>
  <div class="tab-pane" id="php108">
    <pre>
$id = '1234';
$api->get('/ssl.json/'.$id);</pre>
  </div>
  <div class="tab-pane" id="node108">
  <pre>
var id = '1234'
api.get('/ssl.json/' + id, callback)
function callback(err, response) {
  if (err) return console.log(err)
  console.log(response)
}</pre>
  </div>
  <div class="tab-pane" id="java108">
  <pre>String sslId = "1234";
MaxCDNObject response = api.get("/ssl.json/"+sslId));
Console.log(response.error ? "Error " + response.getErrorMessage()  : response.code);</pre>
  </div>
  <div class="tab-pane" id="response108">
    <pre>
{
    "code": 200,
    "data": {
       "ssl": 
            {
                "id": "1234",
                "company_id": "42",
                "domain": "*.example.com",
                "zone_count": "5",
                "date_updated": "2013-05-15 17:33:09",
                "date_expiration": "2015-11-15",
                "ssl_cabundle": "",
                "globalsign": "0",
                "wilcard": "1",
                "ssl_crt": "-----BEGIN CERTIFICATE-----\n...-----END CERTIFICATE-----",
                "name": "Our *.example.com wildcard"
            }
        }
    }
}</pre>
  </div>
</div>

## Update SSL Certificate

Updates an SSL Certificate specified by the {user_id} parameter 

<div class="heading">
<div class="url PUT"><span class="http_method">PUT</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/users.json/{user_id}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`ssl_crt` | - | <span class="label important">required</span><br />length: text; | Certificate  |
`ssl_key` | - | <span class="label important">required</span><br />length: text | Certificate Private Key |
`ssl_cabundle` | - | length: text | Certificate Authority Intermediate Bundle |
`name` | auto_{domain}_{expiration}_{update} | length: 1-255 | Use descriptive name |
`force` | 0 | digit | Override check to ensure that the domain has not changed | 

### Response Parameters

Parameter | Description |
--- | --- | ---
`ssl` | The information about the certificate (see List Certificates response)|


### Code Samples

<ul class="nav nav-tabs" id="myTab109">
  <li class="active"><a href="#ruby109" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python109" data-toggle='tab'>Python</a></li>
  <li><a href="#perl109" data-toggle='tab'>Perl</a></li>
  <li><a href="#php109" data-toggle='tab'>PHP</a></li>
  <li><a href="#node109" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp109" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#java109" data-toggle='tab'>Java</a></li>
  <li><a href="#response109" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby109">
  <pre>
id = '1234'
params={"ssl_crt"=>"-----BEGIN CERTIFICATE-----\n{ you certificate info }\n-----END CERTIFICATE-----","ssl_key"=>"-----BEGIN RSA PRIVATE KEY-----\n{ your private key info}\n-----END RSA PRIVATE KEY-----","ssl_cabundle"=>"-----BEGIN CERTIFICATE.....", "name"=>"Our *.example.com wildcard"}
api.put('/ssl.json/'+id,params)
</pre>
  </div>
  <div class="tab-pane" id="python109">
    <pre>
api.put('/ssl.json/'+id,params={ 'ssl_crt':"-----BEGIN CERTIFICATE-----\n{ you certificate info }\n-----END CERTIFICATE-----",'ssl_key':"-----BEGIN RSA PRIVATE KEY-----\n{ your private key info}\n-----END RSA PRIVATE KEY-----",'ssl_cabundle':"-----BEGIN CERTIFICATE.....",'name':"Our new *.example.com wildcard" })</pre>
  </div>
  <div class="tab-pane" id="perl109">
    <pre>
my $id = 1234;
my @params = ('ssl_crt=-----BEGIN CERTIFICATE-----\n{ you certificate info }\n-----END CERTIFICATE-----', 'ssl_key=-----BEGIN RSA PRIVATE KEY-----\n{ your private key info}\n-----END RSA PRIVATE KEY-----","ssl_cabundle"=>"-----BEGIN CERTIFICATE.....', 'name=Our.example.com-wildcard');
$api->put("/ssl.json/" . $id, @params);
</pre>
  </div>
  <div class="tab-pane" id="php109">
    <pre>
$id = '1234';
$params = array("ssl_crt"=>"-----BEGIN CERTIFICATE-----\n{ you certificate info }\n-----END CERTIFICATE-----","ssl_key"=>"-----BEGIN RSA PRIVATE KEY-----\n{ your private key info}\n-----END RSA PRIVATE KEY-----","ssl_cabundle"=>"-----BEGIN CERTIFICATE.....", "name"=>"Our *.example.com wildcard");
$api->put('/ssl.json/'.$id,$params);</pre>
</div>
  <div class="tab-pane" id="node109">
  <pre>
var id = '1234'
api.put('/ssl.json/' + id, { ssl_crt:"-----BEGIN CERTIFICATE-----\n{ you certificate info }\n-----END CERTIFICATE-----",ssl_key:"-----BEGIN RSA PRIVATE KEY-----\n{ your private key info}\n-----END RSA PRIVATE KEY-----",ssl_cabundle:"-----BEGIN CERTIFICATE.....",name:"Our *.example.com wildcard" }, callback)
function callback(err, response) {
  if (err) return console.log(err)
  console.log(response)
}</pre>
  </div>
  <div class="tab-pane" id="csharp109">
  <pre>
var cert = "";
var key = "";
Console.Write("Zone id: \n");
int zoneId = Convert.ToInt32(Console.ReadLine());
Console.Write("Zone type: \n");
string type = Console.ReadLine();
using (StreamReader sr = new StreamReader("cert.txt"))
{
cert = sr.ReadToEnd();               
}
using (StreamReader sr = new StreamReader("key.txt"))
{
key = sr.ReadToEnd();
}

var dat = "";
cert = "-----BEGIN CERTIFICATE-----\n" + cert + "\n-----END CERTIFICATE-----\n";
key = "-----BEGIN RSA PRIVATE KEY-----\n" + key + "\n-----END RSA PRIVATE KEY-----\n";

api.Put("/ssl.json/" + zoneID, dat="ssl_crt=" + cert + "&ssl_key=" + key);
</pre>
  </div>
  <div class="tab-pane" id="java109">
  <pre>String sslId = "1234";
String ssl_crt = "-----BEGIN CERTIFICATE-----\n{ ... your certificate ... }\n-----END CERTIFICATE-----\n";
String ssl_key = "-----BEGIN RSA PRIVATE KEY-----\n{ ... your key ... }\n-----END RSA PRIVATE KEY-----";
MaxCDNRequest data = MaxCDN.newRequest("ssl_crt", "ssl_crt").append("ssl_key", "ssl_key");
MaxCDNObject response = api.put("/ssl.json"+sslId, data);
Console.log(response.error ? "Error " + response.getErrorMessage()  : response.code);</pre>
</div>
  <div class="tab-pane" id="response109">
    <pre>
{
    "code": 200,
    "data": {
      "ssl": 
            {
                "id": "1234",
                "company_id": "42",
                "domain": "*.example.com",
                "zone_count": "5",
                "date_updated": "2013-05-15 17:33:09",
                "date_expiration": "2015-11-15",
                "ssl_cabundle": "",
                "globalsign": "0",
                "wilcard": "1",
                "ssl_crt": "-----BEGIN CERTIFICATE-----\n...-----END CERTIFICATE-----",
                "name": "Our *.example.com wildcard"
            }
    }
}</pre>
  </div>
</div>

## Delete SSL Certificiate

Deletes a certificate specified by the {ssl_id} parameter

<div class="heading">
<div class="url DELETE"><span class="http_method">DELETE</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/ssl.json/{ssl_id}</span></div>
</div>


### Code Samples

<ul class="nav nav-tabs" id="myTab110">
  <li class="active"><a href="#ruby110" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python110" data-toggle='tab'>Python</a></li>
  <li><a href="#perl110" data-toggle='tab'>Perl</a></li>
  <li><a href="#php110" data-toggle='tab'>PHP</a></li>
  <li><a href="#node110" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp110" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#java110" data-toggle='tab'>Java</a></li>
  <li><a href="#response110" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby110">
    <pre>
id = '1234'
api.delete('/ssl.json/'+id)</pre>
  </div>
  <div class="tab-pane" id="python110">
    <pre>
id = '1234'
api.delete('/ssl.json/'+id)</pre>
  </div>
    <div class="tab-pane" id="perl110">
      <pre>
my $id = 1234;
$api->delete("/ssl.json/" . $id);</pre>
    </div>
  <div class="tab-pane" id="php110">
    <pre>
$id = '1234';
$api->delete('/ssl.json/'.$id);</pre>
  </div>
  <div class="tab-pane" id="node110">
  <pre>
var id = '1234'
api.delete('/ssl.json/' + id, callback)
function callback(err, response) {
  if (err) return console.log(err)
  console.log(response)
}</pre>
  </div>
  <div class="tab-pane" id="csharp110">
  <pre>
Console.Write("Zone id: \n");
int zoneId = Convert.ToInt32(Console.ReadLine());

api.Delete("/ssl.json/" + zoneId);
</pre>
  </div>
  <div class="tab-pane" id="java110">
  <pre>String sslId = "1234";
MaxCDNObject response = api.delete("/ssl.json/"+sslId));
Console.log(response.error ? "Error " + response.getErrorMessage()  : response.code);</pre>
</div>
<div class="tab-pane" id="response110">
    <pre>
{
  "code":200
}</pre>
  </div>
</div>

