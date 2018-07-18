# Laravel-One-to-One-Eloquent-Relationship

+ Retrieve Records:
$phone = User::find(1)->phone;
dd($phone);

$user = Phone::find(1)->user;
dd($user);

---------------------------------------

+ Create Records:
$user = User::find(1);
 
$phone = new Phone;
$phone->phone = '9429343852';
 
$user->phone()->save($phone);

---------------------------------------

$phone = Phone::find(1);
 
$user = User::find(10);
 
$phone->user()->associate($user)->save();


