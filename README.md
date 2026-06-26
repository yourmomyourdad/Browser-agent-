the jitterBug project is an adaptive jitter buffer designed in javascript and modeled after netEq it's split into 3 parts which I will be writing them in the order they're used 
1.packetHolder this is updated in realtime by the backend the only actual code it executes is replacing the time it was sent with the sum of the time it was sent and the time it actually arrived as the departureTime
2.DelayManager this uses how long the average departureTime is for each packet and uses that to decide how long it needs to buffer for optimizing the audio stream 
3.dragSpeed this is a relatively simple part of the project it just sets each slice to last until the next slice is scheduled to activate
