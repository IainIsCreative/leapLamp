# Servo API

- min()

 set the servo to the minimum degrees
 defaults to 0

 eg. servo.min();


- max()

 set the servo to the maximum degrees
 defaults to 180

 eg. servo.max();

- center()

 centers the servo to 90°

  servo.center();

- move( deg )

 Moves the servo to position by degrees

 servo.move( 90 );

- sweep( obj )

 Perform a min-max cycling servo sweep (defaults to 0-180)
 optionally accepts an object of sweep settings:
 {
    lapse: time in milliseconds to wait between moves
           defaults to 500ms
    degrees: distance in degrees to move
           defaults to 10°
 }

 servo.sweep();


# Servo Event API

- "move" events fire after a successful move.
  servo.on("move", function( err, degrees ) {
    console.log( "move", degrees );
  });