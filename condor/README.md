Here a simple example to submit a job to htcondor (Marconi@Cineca)

Setup:
- since proxy available then -> export _condor_SEC_CLIENT_AUTHENTICATION_METHODS=GSI

submission:
> condor_submit -pool CE_AT_CINECA:CE_PORT -remote CE_AT_CINECA -spool p308.sub

check queue:
> condor_q -name CE_AT_CINECA -pool CE_AT_CINECA:CE_PORT

retrive output:
> condor_transfer_data -name CE_AT_CINECA -pool CE_AT_CINECA:CE_PORT JOBID
or
> ./fetchoutput.sh JOBID

