https://www.youtube.com/watch?v=245IboC9Lao homework 1 
https://www.youtube.com/watch?v=b4FHiz1D-Kc homework 2





img = cv2.imread('IMG_6504.jpg')
rows,cols,ch = img.shape
pts1 = np.float32([[171,187],[758,193],[806,1041],[100,1042]])
pts2 = np.float32([[300,300],[800,300],[800,600],[300,600]])
M = cv2.getPerspectiveTransform(pts1,pts2)
dst = cv2.warpPerspective(img,M,(1100,900))
plt.subplot(121),plt.imshow(img),plt.title('Input')
plt.subplot(122),plt.imshow(dst),plt.title('Output')
plt.show()
