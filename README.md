```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((500, 500, 3), dtype=np.uint8)
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Open and Close', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
kernel = np.ones((3, 3), np.uint8)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Input Image with Text")
plt.axis('off')
(-0.5, 499.5, 499.5, -0.5)
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  
plt.title("Opening Operation")
plt.axis('off')
(-0.5, 499.5, 499.5, -0.5)
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
```
