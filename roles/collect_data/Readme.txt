A simple playbook to gather following facts:
- whether certain RPM is installed / its version if exist
- values from certain kernel parameters.

In order to run it e.g.:
ansible-playbook -i ../Hosts collect_data.yml -v > dwh_prod_fmo.csv

In order to make the data excel-friendly:
cat dwh-prod-fmo.csv |sed 's/\[//g; s/\]//g; s/=/,/g; s/>//g; s/"//g; s/false:true//; s/ok://g; s/failed://g; s/(item//g; s/ignoring...//g; s/)//g' > dwh-prod-fmo-nomalized.csv

for i in *.csv; do cat $i |sed 's/\[//g; s/\]//g; s/=/,/g; s/>//g; s/"//g; s/false:true//; s/ok://g; s/failed://g; s/(item//g; s/ignoring...//g; s/)//g' > $i-normalized.csv; done
