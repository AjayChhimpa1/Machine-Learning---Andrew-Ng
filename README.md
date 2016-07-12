# Machine-Learning---Andrew-Ng
Machine Learning - Stanford University - Andrew Ng

My solutions to programming assignments of MOOC ---> Machine Learning by AndrewNg


##For submission error:- "urlread: peer certificate..." issue, and also some other types of "urlread" errors
<br>
Replace line no. 66 in file ===>> (lib/submitWithConfiguration.m)<br>
responseBody = urlread(submissionUrl, 'post', params);
<br>
by this:<br>
[code, responseBody] = system(sprintf('echo jsonBody=%s | curl -k -X POST -d @- %s', body, submissionUrl));

