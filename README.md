# step-ca-pfsense
pfSense support for smallstep CA

The patch fixes the [problem](https://redmine.pfsense.org/issues/9833) with obtaining a certificate from **small-ca** and changes the minimum certificate renewal period.

Updating certificates in my case has been resolved through a custom cron task.

<em>16	*/12	*	*	*	root	/usr/local/pkg/acme/acme_command.sh "renewall" 2>&1 | /usr/bin/logger -t ACME
