# Get Directions with a Google Map

A jQuery plugin that instantiates a Google Map with a Home Location and allows users to request directions on how to get there.

Check out the [LIVE DEMO](http://examples.mikevsweb.com/get-directions-with-google-maps/)

Still needs some improvement for implementation like remove of class dependencies, 'type' not working and the form should have a Reset button. Use at own risk.

### Installing

Where the Google Maps API is requested you will need to add your own [API Key](https://developers.google.com/maps/documentation/javascript/get-api-key).

```HTML
<script type="text/javascript" src="//maps.googleapis.com/maps/api/js?key={your-api-key}">
```

The following will need to be added after jQuery has loaded. This will be the Home location on the map.

```javascript
$('#FindMeOnGoogleMap').GetDirectionsWithGoogleMaps({
    name: 'Awesome Store',
    description: 'A place where you buy awesome stuff for your awesome lifestyle',
    latitude: 48.424050,
    longitude: -123.357708,
    type: 'ROADMAP', 
    zoom: 13
});
```

For it to work like the [demo](http://examples.mikevsweb.com/get-directions-with-google-maps/), you will need to copy over the following HTML:

```HTML
<div id="FindMeOnGoogleMap">						
    <div class="controls columns">						
        <div class="column is-one-third">
            <h3 class="is-size-3">I want to get there by</h3>
            <div class="select is-large">
                <select name="select">
                    <option value="BICYCLING">Bicycling</option> 
                    <option value="DRIVING" selected>Driving</option>
                    <option value="TRANSIT">Transit</option>
                    <option value="WALKING">Walking</option>
                </select>
            </div>
        </div> 
        <div class="column is-two-thirds">
            <div class="field">
                <div class="control">
                    <input class="input is-info" type="text" name="FindMeOnGoogleMapStart" id="FindMeOnGoogleMapStart" placeholder="Enter Address, Postal Code, City, etc." onclick="document.getElementById(this.id).value= '';">
                </div>
            </div>
            <div class="field is-grouped">
                <div class="control">
                    <button class="calculate button is-link">Submit</button>
                </div>
                <div class="control">
                    <button class="reset button is-info">Reset</button>
                </div>
            </div>
        </div>
    </div>
    <div id="map"></div>
</div>	
```

## Built With

* [jQuery](https://jquery.com/) - a fast, small, and feature-rich JavaScript library
* [Google Maps](https://cloud.google.com/maps-platform/) - bring the real world to your users with static and dynamic maps, Street View imagery, and 360° views.
* [Bulma](https://bulma.io) - a free, open source CSS framework based on Flexbox

## Authors

* **Michael C. Breuer** - *Initial work* - [michabre](https://github.com/michabre)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
