# asterisk-dial-PDD-timeout
For those who are looking for PDD timeout during Asterisk Dial application.
This is the smallest and the easiest patch I could create.
I just use the timeout option (second argument) of Dial application.
If you set the timeout value to 1-119 (in seconds), the argument will be applied as PDD timeout.
The PDD timer is removed in case of ringing or progress arrived. 
The timeout is not removed exactly. It is just prolonged to 120 second and used as original timeout option.

When you set the option to 2 (2 seconds)
The Dial will wait two seconds for ringing or progress. 
If none of them arrive in the time, the Dial is ended with hangup cause 41.
Then you can just check ${HANGUPCAUSE} and use another Dial if you want.

There are just two patches for two different asterisk versions I use.
But the patch is so easy so you can create it for your own version of asterisk.

Vit
