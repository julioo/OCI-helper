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
