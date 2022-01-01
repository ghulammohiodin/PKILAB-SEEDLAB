# PKILAB-SEEDLAB
# instructions PDF
https://seedsecuritylabs.org/Labs_16.04/PDF/Crypto_PKI.pdf

# Task 1: Becoming a Certificate Authority (CA)
Copy the configuration file into current directory:

     cp /usr/lib/ssl/openssl.cnf ./openssl.cnf 
   what does this comand means
     
         req	Creates a signing request.
        -new	Creates new requests.
       -x509	Inspects signed certificate by loading x509 modules.
       -keyout	Used to give a path to a filename, where it writes newly created private keys. 
       -out	Specifies the output file where the result will be stored
       -config	Configuration file to be specified. 

create new sub-directories and files 
     
       mkdir PKI
       cp "/usr/lib/ssl/openssl.cnf" "/home/seed/PKI/"
       mkdir demoWK
       cd demoWK
       mkdir certs crl newcerts
       touch 1000 > serial
       gedit index.txt
  https://github.com/ghulammohiodin/PKILAB-SEEDLAB/blob/91c23f19cf6cfe5b205d0789d6d320b3585d1c14/task_1%20pki.png
  https://github.com/ghulammohiodin/PKILAB-SEEDLAB/blob/75734d4870c3b01215b64dd5051e1629a1584456/task_1_1pki.png

Start to generate the self-signed certificate for the CA:

return to the parent directory

     cd ..
    openssl req -new -x509 -keyout ca.key -out ca.crt -config openssl.cnf 
    
      
      Generating a 2048 bit RSA private key
      ...................+++
         .............................................................................+++
      writing new private key to 'ca.key'
     Enter PEM pass phrase:
     Verifying - Enter PEM pass phrase:
     -----
    You are about to be asked to enter information that will be incorporated
    into your certificate request.
    What you are about to enter is what is called a Distinguished Name or a DN.
    There are quite a few fields but you can leave some blank
    For some fields there will be a default value,
    If you enter '.', the field will be left blank.
    -----
    Country Name (2 letter code) [AU]:pk
     State or Province Name (full name) [Some-State]:Panjab
    Locality Name (eg, city) []:swl
    Organization Name (eg, company) [Internet Widgits Pty Ltd]:uosahiwal
    Organizational Unit Name (eg, section) []:uosahiwalbscs
     Common Name (e.g. server FQDN or YOUR name) []:mohiodin
      Email Address []:mohiodin@test.com




 
