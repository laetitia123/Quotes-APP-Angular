### Hello {{$user->legal_first_name}}
You are receiving this email because you requested more information to help you log into one of the MurugoCloud websites or services.
Here is that info with instructions to help you log in below.<br>
Your Murugo.Cloud User Info:
<br><br>
Murugo Name : {{$user->name}}
<br>
First Name : {{$user->legal_first_name}}
<br>
Second Name : {{$user->legal_second_name}}
<br>
Login ID (used to log in): {{$user->loginID}}
<a href="#" style="background-color: #4CAF50; color: white; padding: 10px 20px; text-align: center; text-decoration: none; display: inline-block; border-radius: 5px; font-size: 16px; margin: 4px 2px; cursor: pointer;"> Click me</a>

<button href="{{ route('password.reset', ['token' => $token, 'email' => $user->email]) }}" style="color:red">Reset Password</button>

This password reset link will expire in 60 minutes.<br>
This email was generated from a user clicking on the ‘request ID/PW reset’ link during the login at {{$application->app_name ?? "Murugo.Cloud"}}. No further action is required if you did not request a password reset.
<br><br>
Regards,<br>
MurugoCloud Service Team<br><br><br>
If you’re having trouble clicking the “Reset Password” button, copy and paste the URL below into your web browser:<br>
<a href="{{ route('password.reset', ['token' => $token, 'email' => $user->email]) }}" class="btn btn-link resetpwd-button">{{ route('password.reset', ['token' => $token, 'email' => $user->email]) }}</a>
