#gyro.js

gyro.js is an adaptor which combines all the current interfaces and standards on reading Gyro and Accelerometer information and combines them into one simple object.

## Tested Compatability
	iPhone >= iOS 4.x
	Chrome >= 12.x
	Firefox >= 4.x

## Installation
Copy the file js/gyro.js to your web server or download from <http://www.tomg.co/gyrojs>.

	<script src="js/gyro.js"></script>

## Usage

At the bottom of your document after the including of gyro.js add the following.
	
	<script>
		gyro.startTracking(function(o) {
			// o.x, o.y, o.z for accelerometer
			// o.alpha, o.beta, o.gamma for gyro
		});
	</script>

## API

- `gyro.frequency = 500` - How often to poll for changes.
- `gyro.getOrientation()` - Get the current accelerometer and gyro information.
- `gyro.startTracking(function(o){...})` - Return the gyro data at the specified frequency defined in `gyro.frequency`
- `gyro.stopTracking()` - Clear the interval set in `gyro.startTracking`.
- `gyro.hasFeature('devicemotion')` - Check if the web browser supports either MozOrientation, devicemotion or deviceorientation
- `gyro.getFeatures()` - Gets all accelerometer and gyro features supported.

