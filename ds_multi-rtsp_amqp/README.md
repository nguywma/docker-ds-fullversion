# ds_multi-rtsp_amqp
Deepstream python app for inference with rtsp stream and send message via rabbitmq
All code in here assume that the nvinfer config file path is 
```
/home/ivsr/DeepStream-Yolo/config_infer_primary_yoloV5.txt
```
And the amqp config file is in the running directory
```
amqp_config.txt
```
If not, please change the "PGIE_CONFIG_FILE" and "MSGCONV_CONFIG_FILE" to the right path.
## all-in-one.py
Python code based on deepstream-test1, deepstream-imagedata-multistream and deepstream-rtsp-in-rtsp-out for real-time rtsp inference, saving frame, sending message to rabbitmq and output a rtsp stream. 
To run the code(sudo if nessesary): 
```bash
python3 all-in-one.py rtsp://username:password@address/
```
Example:  
```bash
sudo python3 all-in-one.py rtsp://admin:ivsr2019@192.168.0.103/
```

## detect.py and server.py 
Same as all-in-one but the output is not rtsp 
To run: 
```bash
python3 server.py rtsp://username:password@address/
```

## rtsp.py 
Output message and rtsp only 
```bash
sudo python3 rtsp.py rtsp://admin:ivsr2019@192.168.0.103/
``` 
The output rtsp can be found at 
```
rtsp://localhost/ds-test 
```

