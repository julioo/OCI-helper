# OCI-helper
OCI useful commands and stuff

# List OCI Regions
A list of all the region names and locations for Azure

## Create the list
You can recreate the list anytime using this command:

```sh
oci iam region list --output table
```

## Result
```sh
+-----+-------------------+
| key | name              |
+-----+-------------------+
| AMS | eu-amsterdam-1    |
| ARN | eu-stockholm-1    |
| AUH | me-abudhabi-1     |
| BOM | ap-mumbai-1       |
| CDG | eu-paris-1        |
| CWL | uk-cardiff-1      |
| DXB | me-dubai-1        |
| FRA | eu-frankfurt-1    |
| GRU | sa-saopaulo-1     |
| HYD | ap-hyderabad-1    |
| IAD | us-ashburn-1      |
| ICN | ap-seoul-1        |
| JED | me-jeddah-1       |
| JNB | af-johannesburg-1 |
| KIX | ap-osaka-1        |
| LHR | uk-london-1       |
| LIN | eu-milan-1        |
| MAD | eu-madrid-1       |
| MEL | ap-melbourne-1    |
| MRS | eu-marseille-1    |
| MTY | mx-monterrey-1    |
| MTZ | il-jerusalem-1    |
| NRT | ap-tokyo-1        |
| ORD | us-chicago-1      |
| PHX | us-phoenix-1      |
| QRO | mx-queretaro-1    |
| SCL | sa-santiago-1     |
| SIN | ap-singapore-1    |
| SJC | us-sanjose-1      |
| SYD | ap-sydney-1       |
| VCP | sa-vinhedo-1      |
| YNY | ap-chuncheon-1    |
| YUL | ca-montreal-1     |
| YYZ | ca-toronto-1      |
| ZRH | eu-zurich-1       |
+-----+-------------------+
```

# Install ADBping
## Install requirement
Use Oracle Linux
```sh
sudo dnf install oracle-instantclient-release-el8 -y
sudo dnf install oracle-instantclient-basic -y
sudo dnf install oracle-instantclient-sqlplus -y
sudo dnf install java-11-openjdk-devel -y
sudo dnf install tzdata-java -y
```

## Install adbping
```sh
wget https://objectstorage.us-ashburn-1.oraclecloud.com/p/roSMTyBAHgIHlbEgWfHE-DFCVTAS5eFkqW9xuPCTM8zYEyFNVvIZFjCdk67gN5Fj/n/nrwchkxcfasu/b/adbping/o/adbping_Linux.X64_230127.zip
mkdir adbping
mv adbping_Linux.X64_230127.zip adbping
cd adbping
unzip adbping_Linux.X64_230127.zip
```

## Use adbping

### With BaseDB
Create adbping user
```sh
sqlplus sys/"password"@easy_connect as sysdba
SQL>create user adbping identified by password;
SQL>grant create session to adbping;
```
```sh
 ./adbping -u adbping -p password -c java -w /tmp -s easy_connect
```
