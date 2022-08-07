# Protocol

- `python demo_darknet2onnx.py phth_experiments/yolov4_to_onnx/yolov4-tiny_training.cfg phth_experiments/yolov4_to_onnx/signs.names.txt phth_experiments/yolov4_to_onnx/yolov4-tiny_training_last.weights phth_experiments/yolov4_to_onnx/yolo_traffic_signs_test_image.jpg 64` hat funktioniert!
  - in `pytorch-YOLOv4/tool/utils.py` wurde folgendes geändert:
    ```python
    140             # phth:
    141 #            cv2.rectangle(img, (x1,y1), (np.float32(c3[0]), np.float32(c3[1])), rgb, -1)
    142 #            img = cv2.putText(img, msg, (c1[0], np.float32(c1[1] - 2)), cv2.FONT_HERSHEY_SIMPLEX,0.7, (0,0,0), bbox_thick//2,lineType=cv2.LINE_AA)
    143             cv2.rectangle(img, (int(x1),int(y1)), (int(np.float32(c3[0])), int(np.float32(c3[1]))), rgb, -1)
    144             img = cv2.putText(img, msg, (int(c1[0]), int(np.float32(c1[1] - 2))), cv2.FONT_HERSHEY_SIMPLEX,0.7, (0,0,0), bbox_thick//2,lineType=cv2.LINE_AA    )
    ```
- `yolov4-tiny_training.cfg` und `yolov4-tiny_training_last.weights` sind aus `/home/bra-ket/git/Galaxis/ws_270322_trafficsign/Traffic-Signs-Detection-Tensorflow-YOLOv3-YOLOv4`
