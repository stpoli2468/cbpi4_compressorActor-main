# Compressor-plugin for cbpi4

This plugin adds Actors for controlling compressors (like refridgerators/freezers). To prevent damage to the compressor, you should not turn the compressor on and off repeatedly. It's best to have a delay between cycles. This actor allows for that delay.

There are two types of compressor
- GPIOCompressor: A GPIO compressor actor with parameter to decide if GPIO should be inverted or not.
- MQTTCompressor: A MQTT compressor actor to prevent many switches on MQTT devices.

Both accept a number of minutes to delay before allowing turning the compressor back on again. 
The timer-value for switch-on is possible can be displayed in the newest craftbeerpi4-ui version.

If actor is triggered before delaytime is elapsed, triggering will be remember and actived after delaytime is reached.