
## Hello {{$user->legal_first_name}}
You are receiving this email because you requested more information to help you log into one of the MurugoCloud websites or services.
Here is that info with instructions to help you log in below. <br><br>
Your Murugo.Cloud User Info:
<br><br>
Murugo Name : {{$user->name}}
<br>
First Name : {{$user->legal_first_name}}
<br>
Second Name : {{$user->legal_second_name}}
<br>
Login ID (used to log in): {{$user->loginID}}

<button><a href="{{ route('password.reset', ['token' => $token, 'email' => $user->email]) }}" class="btn resetpwd-button-link">Reset Password</a></button>

This password reset link will expire in 60 minutes.<br><br>
This email was generated from a user clicking on the ‘request ID/PW reset’ link during the login at {{$application->app_name ?? "Murugo.Cloud"}}. No further action is required if you did not request a password reset.
<br><br><br><br>
Regards,<br><br>
MurugoCloud Service Team<br><br><br><br>
If you’re having trouble clicking the “Reset Password” button, copy and paste the URL below into your web browser:<br><br>
<a href="{{ route('password.reset', ['token' => $token, 'email' => $user->email]) }}" class="btn btn-link resetpwd-button">{{ route('password.reset', ['token' => $token, 'email' => $user->email]) }}</a>
