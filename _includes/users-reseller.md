# Users API

## List Users

Returns a list of all users on the specified account

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/clients/{id}/users.json</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | User ID |
`email` | Email Address |
`firstname` | First Name |
`lastname` | Last Name |
`phone` | Phone Number |
`timezone` | User's Timezone |
`date_last_login` | The date and time the user last logged into the system |
`ip_last_login` | The IP for the user at the last login |
`date_created` | Date Created |
`date_updated` | Date Updated |
`roles` | An array of roles for the given user |

### Code Samples

<ul class="nav nav-tabs" id="myTab5">
  <li class="active"><a href="#ruby5" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python5" data-toggle='tab'>Python</a></li>
  <li><a href="#perl5" data-toggle='tab'>Perl</a></li>
  <li><a href="#php5" data-toggle='tab'>PHP</a></li>
  <li><a href="#node5" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp5" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response5" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby5">
<pre>
api.get('/clients/{id}/users.json')</pre>
  </div>
  <div class="tab-pane" id="python5">
    <pre>
api.get('/clients/{id}/users.json')</pre>
  </div>
    <div class="tab-pane" id="perl5">
<pre>
my $data = $api->get("/clients/{id}/users.json");
print $data->{'users'}[0]{'id'};</pre>
  </div>
  <div class="tab-pane" id="php5">
<pre>
$api->get('/clients/{id}/users.json');</pre>
  </div>
  <div class="tab-pane" id="node5">
<pre>
api.get('/clients/{id}/users.json', callback)
function callback(err, response) {
  if (err) return console.log(err)
  console.log(response)
}</pre>
  </div>
  <div class="tab-pane" id="csharp5">
<pre>
api.Get("/clients/{id}/users.json");
</pre>
  </div> 
  <div class="tab-pane" id="response5">
    <pre>
{
    "code": 200,
    "data": {
        "current_page_size": 4,
        "page": 1,
        "page_size": "50",
        "pages": 1,
        "total": 4,
        "users": [
            {
                "brand_id": "1",
                "date_created": "2013-05-15 17:32:30",
                "date_last_login": "2013-05-23 17:54:18",
                "date_updated": "2013-05-15 17:33:09",
                "default_company_id": "#####",
                "email": "name@domain.com",
                "firstname": "Given",
                "id": "33706",
                "ip_last_login": "12.13.90.183",
                "isadmin": "0",
                "isdisabled": "0",
                "lastname": "Family",
                "phone": "3235551400",
                "roles": [
                    "User",
                    "Account Owner"
                ],
                "timezone": "Europe/London"
            },
            {
                "brand_id": "1",
                "date_created": "2013-05-15 20:16:34",
                "date_last_login": null,
                "date_updated": "0000-00-00 00:00:00",
                "default_company_id": "19538",
                "email": "caphammer1@hamcave.com",
                "firstname": "Captain",
                "id": "33714",
                "ip_last_login": null,
                "isadmin": "0",
                "isdisabled": "0",
                "lastname": "Hammer",
                "phone": null,
                "roles": [
                    "User"
                ],
                "timezone": "Europe/London"
            },
            {
                "brand_id": "1",
                "date_created": "2013-05-15 20:20:03",
                "date_last_login": null,
                "date_updated": "2013-05-15 20:31:05",
                "default_company_id": "19538",
                "email": "drhorrible3@ele.net",
                "firstname": "Billy",
                "id": "33716",
                "ip_last_login": null,
                "isadmin": "0",
                "isdisabled": "0",
                "lastname": "Horrible",
                "phone": null,
                "roles": [
                    "User"
                ],
                "timezone": "Europe/London"
            }
        ]
    }
}</pre>
  </div>
</div>


## Create User

Creates a new user on the specified account

<div class="heading">
<div class="url POST"><span class="http_method">POST</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/clients/{id}/users.json</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`email` | - | <span class="label important">required</span><br />length: 6-200 chars; valid email address | Email Address |
`password` | - | <span class="label important">required</span><br />length: 5-30 chars | Password |
`firstname` | - | <span class="label important">required</span><br />length: 1-32 chars | First Name |
`lastname` | - | <span class="label important">required</span><br />length: 1-32 chars | Last Name |
`phone` | - | length: 7, 10, 11, or 14 chars; only digits considered | Phone Number |
`timezone` | - | valid::timezone | Valid timezone (see [List of Supported Timezones](http://php.net/manual/en/timezones.php)) |


### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | User ID |
`email` | Email Address |
`firstname` | First Name |
`lastname` | Last Name |
`phone` | Phone Number |
`timezone` | User's Timezone |
`date_last_login` | The date and time the user last logged into the system |
`ip_last_login` | The IP for the user at the last login |
`date_created` | Date Created |
`date_updated` | Date Updated |
`roles` | An array of roles for the given user |


### Code Samples

<ul class="nav nav-tabs" id="myTab6">
  <li class="active"><a href="#ruby6" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python6" data-toggle='tab'>Python</a></li>
  <li><a href="#perl6" data-toggle='tab'>Perl</a></li>
  <li><a href="#php6" data-toggle='tab'>PHP</a></li>
  <li><a href="#node6" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp6" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response6" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby6">
<pre>
params={"email"=>"name44@domain.com","password"=>"password","firstname"=>"Given","lastname"=>"Family"}
api.post('/clients/{id}/users.json',params )</pre>
  </div>
  <div class="tab-pane" id="python6">
<pre>
params={'email':'name43@domain.com','password':'password','firstname':'Given','lastname':'Family'}
api.post('/clients/{id}/users.json',data=params )</pre>
  </div>
    <div class="tab-pane" id="perl6">
<pre>
my @params = {firstname => 'Perl', lastname => 'User', email => 'user@domain.com', password => 'testpwd'};
$api->post("/clients/{id}/users.json", @params);</pre>
  </div>
  <div class="tab-pane" id="php6">
<pre>
$params = array("email"=>"name@domain.com","password"=>"password","firstname"=>"Given","lastname"=>"Family");
$api->post('/clients/{id}/users.json',$params );</pre>
  </div>
  <div class="tab-pane" id="node6">
<pre>
api.post('/clients/{id}/users.json', { email: 'name@domain.com', password: 'password', firstname: 'Given', lastname: 'Family' }, callback)
function callback(err, response) {
  if (err) return console.log(err)
  console.log(response)
}</pre>
  </div>
  <div class="tab-pane" id="csharp6">
<pre>
Console.Write("User First Name: \n");
string fname = Console.ReadLine();
Console.Write("User Last Name: \n");
string lname = Console.ReadLine();
Console.Write("User email: \n");
string email = Console.ReadLine();
Console.Write("Password: \n");
string pwd = Console.ReadLine();

api.Post("/clients/{id}/users.json", "firstname=" + fname + "&lastname=" + lname + "&password=" + pwd + "&email=" + email);
</pre>
  </div> 
  <div class="tab-pane" id="response6">
    <pre>
{
    "code": 201,
    "data": {
        "user": {
            "brand_id": null,
            "date_created": "2013-05-23 18:22:11",
            "date_last_login": null,
            "date_updated": null,
            "default_company_id": "19538",
            "email": "name@domain.com",
            "firstname": "Given",
            "id": 33941,
            "ip_last_login": null,
            "isadmin": 0,
            "isdisabled": 0,
            "lastname": "Family",
            "phone": null,
            "roles": [
                "User"
            ],
            "timezone": "America/Los_Angeles"
        }
    }
}</pre>
  </div>
</div>


## Get User

Gets a user specified by the {user_id} parameter

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/clients/{id}/users.json/{user_id}</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | User ID |
`email` | Email Address |
`firstname` | First Name |
`lastname` | Last Name |
`phone` | Phone Number |
`timezone` | User's Timezone |


### Code Samples

<ul class="nav nav-tabs" id="myTab7">
  <li class="active"><a href="#ruby7" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python7" data-toggle='tab'>Python</a></li>
  <li><a href="#perl7" data-toggle='tab'>Perl</a></li>
  <li><a href="#php7" data-toggle='tab'>PHP</a></li>
  <li><a href="#node7" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp7" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response7" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby7">
<pre>
id = '33706'
api.get('/clients/{id}/users.json/'+id)</pre>
  </div>
  <div class="tab-pane" id="python7">
<pre>
id = '33706'
api.get('/clients/{id}/users.json/' + id)</pre>
  </div>
    <div class="tab-pane" id="perl7">
<pre>
my $id = 58309;
my $data = $api->get("/clients/{id}/users.json/58309");
print $data->{'user'}{'lastname'};</pre>
  </div>
  <div class="tab-pane" id="php7">
<pre>
my $id = 58309;
my $data = $api->get("/clients/{id}/users.json/58309");
print $data->{'user'}{'lastname'};</pre>
  </div>
  <div class="tab-pane" id="node7">
<pre>
var id = '33941'
api.get('/clients/{id}/users.json/' + id, callback)
function callback(err, response) {
  if (err) return console.log(err)
  console.log(response)
}</pre>
  </div>
  <div class="tab-pane" id="csharp7">
<pre>
Console.Write("User ID: \n");
string id = Console.ReadLine();

api.Get("/clients/{id}/users.json/" + id);
</pre>
  </div> 
  <div class="tab-pane" id="response7">
    <pre>
{
    "code": 200,
    "data": {
        "user": {
            "brand_id": "1",
            "date_created": "2013-05-23 18:22:11",
            "date_last_login": null,
            "date_updated": "0000-00-00 00:00:00",
            "default_company_id": "19538",
            "email": "name@domain.com",
            "firstname": "Given",
            "id": "33941",
            "ip_last_login": null,
            "isadmin": "0",
            "isdisabled": "0",
            "lastname": "Family",
            "phone": null,
            "roles": [
                "User"
            ],
            "timezone": "Europe/London"
        }
    }
}</pre>
  </div>
</div>


## Update User

Updates a user specified by the {user_id} parameter

<div class="heading">
<div class="url PUT"><span class="http_method">PUT</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/clients/{id}/users.json/{user_id}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`email` | - | length: 6-200 chars; valid email address | Email Address |
`firstname` | - | length: 1-32 chars | First Name |
`lastname` | - | length: 1-32 chars | Last Name |
`phone` | - | length: 7, 10, 11, or 14 chars; only digits considered | Phone Number |
`timezone` | - | valid::timezone | Valid timezone (see [List of Supported Timezones](http://php.net/manual/en/timezones.php)) |


### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | User ID |
`email` | Email Address |
`firstname` | First Name |
`lastname` | Last Name |
`phone` | Phone Number |
`timezone` | User's Timezone |

### Code Samples

<ul class="nav nav-tabs" id="myTab8">
  <li class="active"><a href="#ruby8" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python8" data-toggle='tab'>Python</a></li>
  <li><a href="#perl8" data-toggle='tab'>Perl</a></li>
  <li><a href="#php8" data-toggle='tab'>PHP</a></li>
  <li><a href="#node8" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp8" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response8" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby8">
<pre>
id = '33706'
params={'firstname'=> 'name'}
api.put('/clients/{id}/users.json/' + id,params)
</pre>
  </div>
  <div class="tab-pane" id="python8">
<pre>
api.put('/clients/{id}/users.json/'+id,params={'firstname': 'name'})</pre>
  </div>
    <div class="tab-pane" id="perl8">
<pre>
my $id = 58309;
my @params = ('lastname=Test');
$api->put("/clients/{id}/users.json/" . $id, @params);</pre>
  </div>
  <div class="tab-pane" id="php8">
<pre>
$id = '33941';
$params =  array("firstname"=>"Billy");
$api->put('/clients/{id}/users.json/'.$id,$params);</pre>
</div>
  <div class="tab-pane" id="node8">
<pre>
var id = '33941'
api.put('/clients/{id}/users.json/' + id, { firstname: 'Billy' }, callback)
function callback(err, response) {
  if (err) return console.log(err)
  console.log(response)
}</pre>
  </div>
  <div class="tab-pane" id="csharp8">
<pre>
Console.Write("Enter user ID to edit: \n");
int uid = Convert.ToInt32(Console.ReadLine());
Console.Write("Enter property to edit: \n");
string prop = Console.ReadLine();
Console.Write("New value: \n");
string val = Console.ReadLine();

api.Put("/clients/{id}/users.json/" + uid + "/", prop + "=" + val);
</pre>
  </div> 
  <div class="tab-pane" id="response8">
    <pre>
{
    "code": 200,
    "data": {
        "user": {
            "brand_id": "1",
            "date_created": "2013-05-23 18:22:11",
            "date_last_login": null,
            "date_updated": "2013-05-23 19:10:09",
            "default_company_id": "19538",
            "email": "name@domain.com",
            "firstname": "Billy",
            "id": "33941",
            "ip_last_login": null,
            "isadmin": "0",
            "isdisabled": "0",
            "lastname": "Family",
            "phone": null,
            "roles": [
                "User"
            ],
            "timezone": "Europe/London"
        }
    }
}</pre>
  </div>
</div>


## Delete User

Deletes a user specified by the {user_id} parameter

<div class="heading">
<div class="url DELETE"><span class="http_method">DELETE</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/clients/{id}/users.json/{user_id}</span></div>
</div>


### Code Samples

<ul class="nav nav-tabs" id="myTab9">
  <li class="active"><a href="#ruby9" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python9" data-toggle='tab'>Python</a></li>
  <li><a href="#perl9" data-toggle='tab'>Perl</a></li>
  <li><a href="#php9" data-toggle='tab'>PHP</a></li>
  <li><a href="#node9" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp9" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response9" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby9">
<pre>
id = '33706'
api.delete('/clients/{id}/users.json/'+id)</pre>
  </div>
  <div class="tab-pane" id="python9">
<pre>
id = '33706'
api.delete('/clients/{id}/users.json/'+id)</pre>
  </div>
    <div class="tab-pane" id="perl9">
<pre>
my $id = 58309;
$api->delete("/clients/{id}/users.json/" . $id);</pre>
  </div>
  <div class="tab-pane" id="php9">
<pre>
$id = '33715';
$api->delete('/clients/{id}/users.json/'.$id);</pre>
  </div>
  <div class="tab-pane" id="node9">
<pre>
var id = '33715'
api.delete('/clients/{id}/users.json/' + id, callback)
function callback(err, response) {
  if (err) return console.log(err)
  console.log(response)
}</pre>
  </div>
  <div class="tab-pane" id="csharp9">
<pre>
Console.Write("User id to delete: \n");
int id = Convert.ToInt32(Console.ReadLine());
api.Delete("/clients/{id}/users.json/" + id);
</pre>
  </div> 
  <div class="tab-pane" id="response9">
    <pre>
{
  "code":200
}</pre>
  </div>
</div>

