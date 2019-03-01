# ISO3166-to-GPS
CSV datatable giving the centroids for all ISO registered countries.

## Dataset Description 
* ISO codes, in alphanumeric2/3 and numeric3 ("alpha2" - "alpha3" - "iso_num")
* Country names, short and full ("shortCountry" - "country")
* The GPS coordinates of the centroids ("lat" - "long")

## Some information

### Data vis 

Here is a small plot generated with the [tmap](https://github.com/mtennekes/tmap) package :

![R tmap plot](https://user-images.githubusercontent.com/20594983/31993216-d2a2a0ca-b97c-11e7-84ea-3f986830ef6a.png)

### Special Cases

* Kosovo is not listed as an ISO standard country. The unofficial 2 and 3-digit codes are used by the European Commission and others until Kosovo is assigned an ISO code. It's still in this datatable but marked with an [UNOFFICIAL] tag.
* Be carefull with Namibia, the Isocode of this country being NA you can have a not defined value if you dont read it properly (reading it using data.table fread: ```fread("<filepath>/iso2gps.csv", na="")```)!

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
