# gcp credentials api restrictions google map api for ios or android
- Key restrictions help prevent unauthorized use and quota theft
- Dont use Google Map API Key with the same project with our proudction project for GKE,CloudSQL etc, create new project for Google Map API for stability

## For IOS
![alt text](https://i.imgur.com/qWIOaRW.png)

![alt text](https://i.imgur.com/vTKWsZU.png)

![alt text](https://i.imgur.com/uQo4eqt.png)

## For Backend access Google Map API
- Allow key only can use in network/vpc gcp, you can ask google cloud support for get block IPv6 in your VPC
![alt text](https://i.imgur.com/mCAvFF0.png)

![alt text](https://i.imgur.com/83w0PaG.png)

#### Test use your key google map from outside gcp network, REQUEST_DENIED because your key only allow from gcp network
```
curl -X GET "https://maps.googleapis.com/maps/api/place/autocomplete/json?input=Tanjung%20Duren%20Selatan,%20Grogol%20Petamburan,%20Jakarta%20Barat,%20DKI%20Jakarta,%20Indonesia&key=your-key-xxxxxx"
{
   "error_message" : "This IP, site or mobile application is not authorized to use this API key. Request received from IP address 106.250.163.24, with empty referer",
   "predictions" : [],
   "status" : "REQUEST_DENIED"
}
```

## Dashboard Google Map
![alt text](https://i.imgur.com/TbHSNVN.png)
