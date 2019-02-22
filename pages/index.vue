<template>
  <section class="container">
    <div>
      <input id="searchTextField" type="text" placeholder="testing">
    </div>
  </section>
</template>

<script>
export default {
	mounted: function () {
		var defaultBounds = new google.maps.LatLngBounds(
		new google.maps.LatLng(-33.8902, 151.1759),
		new google.maps.LatLng(-33.8474, 151.2631));

		var input = document.getElementById('searchTextField');
		var options = {
			bounds: defaultBounds,
			types: ['establishment']
		};

		this.autocomplete = new google.maps.places.Autocomplete(input, options);
	},
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
