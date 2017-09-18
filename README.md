# google-maps-tips
Detalles sobre el uso del api de google maps


## Cómo filtrar los resultados del mapa por país y/o estado
```
    function getUserAddress(address){
        var geocoder = new google.maps.Geocoder();//usamos el geocoder
        
        geocoder.geocode({address, componentRestrictions: {country: 'MX', administrativeArea: 'CDMX'}}, function(results, status) {//lo importante es pasar las componentRestrictions. Más info aquí: https://developers.google.com/maps/documentation/javascript/reference#GeocoderComponentRestrictions
          if (status !== google.maps.GeocoderStatus.OK) { return}
            //hacer algo con results

        });
    }
```
