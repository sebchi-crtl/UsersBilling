# UsersBilling
HollaTags Coding Challenge

# Problem
Problem:
• An application for billing 10,000 users over a given billing API (owned by a third
party e.g. Telco/Bank).
• The billing API takes 1.6secs to process and respond to each request
• The details of the users to bill is stored in a Database with fields; id, username,
mobile_number and amount_to_bill

# Way I'm using in this 
I would run 5 api asynchronously, billing 2250 users in each api till the billing is done.

# Precedures.
if (!empty(username) && !empty(amount_to_bill) ){
SELECT * FROM `category` WHERE category_ID BETWEEN 1 and 2250
then make an asyn call to the api
 $url = "https://******************";
  $fields = [
    'currency' => "NGN",
    'source' => "balance",
    'transfers' => [{
      'amount' => 20000,
      'recipient' => "1st 2250 users"
    {
      'amount' => 20000,
      'reason' =>  "Easy does it",
      'recipient' => "1st 2250 users"
    }]
  ];
  $fields_string = http_build_query($fields);
  //open connection
  $ch = curl_init();
  echo $result;

SELECT * FROM `category` WHERE category_ID BETWEEN 2251 and 4500
then make an asyn call to the api
 url = "https://******************";
  $fields = [
    'currency' => "NGN",
    'source' => "balance",
    'transfers' => [{
      'amount' => 20000,
      'recipient' => "1st 2250 users"
    {
      'amount' => 20000,
      'reason' =>  "Easy does it",
      'recipient' => "1st 2250 users"
    }]
  ];
  $fields_string = http_build_query($fields);
  //open connection
  $ch = curl_init();
  echo $result;
  
SELECT * FROM `category` WHERE category_ID BETWEEN 4501 and 6750  
then make an asyn call to the api
 url = "https://******************";
  $fields = [
    'currency' => "NGN",
    'source' => "balance",
    'transfers' => [{
      'amount' => 20000,
      'recipient' => "1st 2250 users"
    {
      'amount' => 20000,
      'reason' =>  "Easy does it",
      'recipient' => "1st 2250 users"
    }]
  ];
  $fields_string = http_build_query($fields);
  //open connection
  $ch = curl_init();
  echo $result;
  
SELECT * FROM `category` WHERE category_ID BETWEEN 6751 and 9000  
then make an asyn call to the api
 url = "https://******************";
  $fields = [
    'currency' => "NGN",
    'source' => "balance",
    'transfers' => [{
      'amount' => 20000,
      'recipient' => "1st 2250 users"
    {
      'amount' => 20000,
      'reason' =>  "Easy does it",
      'recipient' => "1st 2250 users"
    }]
  ];
  $fields_string = http_build_query($fields);
  //open connection
  $ch = curl_init();
  echo $result;
  
SELECT * FROM `category` WHERE category_ID BETWEEN 9000 and 10000
then make an asyn call to the api
 url = "https://******************";
  $fields = [
    'currency' => "NGN",
    'source' => "balance",
    'transfers' => [{
      'amount' => 20000,
      'recipient' => "1st 2250 users"
    {
      'amount' => 20000,
      'reason' =>  "Easy does it",
      'recipient' => "1st 2250 users"
    }]
  ];
  $fields_string = http_build_query($fields);
  //open connection
  $ch = curl_init();
  echo $result; 
}


# 1.6secs to a user
the api takes 1.6secs 
so proccessing 10,000 users should be rounding up to 4.5hrs 
so breaking it down we know in 1.6secs it can only take 2250 users in 1hr
while 100,000 users will round up to 44.5hrs

# Calculating
1.6secs = 1 user
60secs = 1 min
60mins = 1 hr

so 1 hr to secs
60*60 = 3600
3600 secs = 1hr
 finding how many users the billing can process in an hr
 number of total seconds to users / number of sec to a user = number of users
 3600/1.6 = 2250
 *** an api can only bill 2250 users within an hour
 
 # for 100,000 users in 4.5hrs
 i will use the run it same as the 10,000 user but using 10 api note ** all running asynchronously **
 when 10,000 is 4.5 hrs so in 100,000 we would make use of 10 apis to get to the 4.5 hrs
 
 # Running asynchronously
 We can also make it run in mins with more api calls to the third party 
