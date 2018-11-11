# Change Log

### v4.2.0
* Add the ability to run service handlers when a certificate is updated with **ler53_service_handlers**.

### v4.1.0
* Add the ability to specify extended key usage on CSRs (thanks @calebtonn).

### v4.0.0
* Allow specifying a custom URL to the Let's Encrypt agreement.
* Migrate to the Ansible OpenSSL modules for idempotence (now installs pyOpenSSL).
* Use Python virtualenvs when installing boto and pyOpenSSL on RHEL/CentOS.
* Add the ability to recreate a cert when the CSR changes.

### v3.1.0
* Install prerequisite packages on FreeBSD.
* Add the ability to specify SAN's for the same domain.
* Add the ability specify the key usage.

### v3.0.0
* Install the python-boto package instead of through pip.
* Remove the variables **ler53_cert_country**, **ler53_cert_state**, **ler53_cert_locality**, and **ler53_cert_organization** since these aren't used by Let's Encrypt (thanks @stevenringo).
* Remove the variable **ler53_cert_subject** and now only use **ler53_cert_common_name**.

### v2.0.0
* Replace **ler53_intermediate_download** with **ler53_chain_download**.
* Replace **ler53_intermediate_file_name** with **ler53_chain_file_name**.
* Replace **ler53_cert_and_intermediate_file_name** with **ler53_cert_and_chain_file_name**.
* Default **ler53_cert_file_name** to `{{ ler53_cert_common_name }}.crt`.
* Default **ler53_intermediate_file_name** to `{{ ler53_cert_common_name }}.intermediate.crt`.
* Default **ler53_cert_and_intermediate_file_name** to `{{ ler53_cert_common_name }}.pem`.
* Make ownership and permissions on **ler53_cert_dir** compatible with more *nix systems.

### v1.0.0
* Initial release.
