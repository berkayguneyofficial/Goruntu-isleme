!pip install easyocr
import easyocr as berkay_ocr
import cv2 as berkay_cv2
import numpy as berkay_np

berkay_ocr_motoru = berkay_ocr.Reader(['en', 'tr'])
with open('berkay_resim.jpg', 'rb') as berkay_f:
    berkay_resim = berkay_f.read()
    berkay_resim_ham = berkay_np.fromstring(berkay_resim, berkay_np.uint8)
    berkay_resim_cv2 = berkay_cv2.imdecode(berkay_resim_ham, berkay_cv2.IMREAD_COLOR)
from google.colab.patches import cv2_imshow as berkay_cv2_imshow
berkay_cv2_imshow(berkay_resim_cv2)
berkay_yazilar = berkay_ocr_motoru.readtext(berkay_resim)
for berkay_yazi in berkay_yazilar:
    print(berkay_yazi)
for berkay_yazi in berkay_yazilar:
    berkay_pt1 = (int(berkay_yazi[0][0][0]), int(berkay_yazi[0][0][1]))
    berkay_pt2 = (int(berkay_yazi[0][2][0]), int(berkay_yazi[0][2][1]))
    berkay_cv2.rectangle(berkay_resim_cv2, berkay_pt1, berkay_pt2, (0, 0, 255), 2)
from google.colab.patches import cv2_imshow as berkay_cv2_imshow
berkay_cv2_imshow(berkay_resim_cv2)
