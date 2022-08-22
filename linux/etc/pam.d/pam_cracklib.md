## pam_cracklib - PAM module to check the password against dictionary words

## SYNOPSIS

pam_cracklib.so [...]

## OPTIONS
retry=N
	Prompt user at most N times before returning with error. The default is 1.

difok=N
	This argument will change the default of 5 for the number of character changes in the new password that differentiate it from the old password.

minlen
	The minimun acceptable size for the new password

dcredit=N
	(N >= 0) This is the maximun credit for having digits in the new password.
	(N < 0) This is the minimun number of digits that must be met for a new password.

ucredit=N
	(N >= 0) This is the maximun credit for having upper case letters in the new password.
	(N < 0) This is the minimun number of upper case letters that must be met for a new password.

lcredit=N
	(N >=0 ) This is the maximun credit for having lower case letters in the new password.
	(N < 0) This is the minumum number of lower case letters that must be met for a new password.

maxrepeat=N
	Reject passwords which contain more than N consecutive characters. The default is 0 which means that this check is disabled.

reject_username
	Check whether the name of the user in straight or reversed from is contained in the new password. If it is found the new password is rejected

enforce_for_root
	The module will return error on failed check also if the user changing the password is root.

## SEE ALSO
[[pam]]

---

#password

man 8 pam_cracklib