import cv2
 capture = cv2.VideoCapture("play.mp4")
 if capture.isOpened() is False:
 print("Error opening video")
 frame_idx = capture.get(cv2.CAP_PROP_FRAME_COUNT)-1
 print("Starting Frame: '{}'".format(frame_idx))
 while capture.isOpened() and frame_idx >= 0:
 capture.set(cv2.CAP_PROP_POS_FRAMES, frame_idx)
 ret, frame = capture.read()
 if ret is True:
 cv2.imshow('Frame in Reverse', frame)
 frame_idx = frame_idx- 1
 print("Next index: '{}'".format(frame_idx))
 if cv2.waitKey(30) == ord('q'):
 break
 else:
 break
 capture.release()
 cv2.destroyAllWindows()
