# ISO3166-to-GPS
CSV datatable giving the center point for all ISO registered Country.

## Dataset Description 
* The ISOcodes in alphanumeric2/3 and numeric3 ("alpha2" - "alpha3" - "iso_num")
* Country names, short and full ("shortCountry" - "country")
* The GPS coordinates of the middle points ("lat" - "long")

## Getting Started

These instructions will get you the database loaded in R environnement

### Installing

First, I highly suggest you to use the data.table package. data.table provide you a good and fast csv reader (fread). You should install and load the necessary package:

```
install.packages("data.table")
library(data.table)
```

Then, we use fread to load the dataset in a data.table (much faster than a data.frame for big amount of data). We use - na="" - for the special case of Namibia (see below):

```
my_dt <- fread("<filepath>/iso2gps.csv", na="")
```

We now have the data in our R environement. Here is a small plot generate with the [tmap](https://github.com/mtennekes/tmap) package :

* WIP

### Special Cases

* Kosovo is not listed as an ISO standard country. The unofficial 2 and 3-digit codes are used by the European Commission and others until Kosovo is assigned an ISO code. It's still in this datatable but marked with an [UNOFFICIAL] tag.
* Be carefull with Namibia, the Isocode of this country being NA you can have a not defined value if you dont read it properly !

## Contributing

If you want to help, just commit more precise coordinates !
Commit without an explicit name and a list of changes will be rejected

## Authors

* **Milo Parigi** - [Github](https://github.com/MiloParigi)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Credit

This file is based on data from [here](http://www.arcgis.com/home/item.html?id=f4d8f9131fe6411f8da592208fbe5ddc)
