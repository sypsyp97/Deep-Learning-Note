import numpy as np
import matplotlib.pyplot as plt


class Checker:
    def __init__(self, resolution, tile_size):
        self.resolution = resolution
        self.tile_size = tile_size
        self.output = np.zeros((resolution, resolution), dtype = np.int8)

    def draw(self):
        self.output[1::2, 0::2] = 1
        self.output[0::2, 1::2] = 1
        
        return self.output.copy()

    def show(self):
        plt.xticks([])
        plt.yticks([])
        plt.imshow(self.output, cmap='gray')
        plt.show()
        


class Circle:
    def __init__(self, resolution, radius, position):
        self.resolution = resolution
        self.radius = radius
        self.pos_x, self.pos_y = position
        self.output = np.zeros((resolution, resolution), dtype = np.int8)
        
    def draw(self):
        for i in range(self.pos_x + self.radius + 1):
            for j in range(self.pos_y + self.radius + 1):
                if (self.pos_x - i)**2 + (self.pos_y - j)**2 <= (self.radius)**2:
                    self.output[i, j] = 1
        
        return self.output.copy()
        
    def show(self):
        plt.xticks([])
        plt.yticks([])
        plt.imshow(self.output, cmap='gray')
        plt.show()

    

class Spectrum:
    def __init__(self, resolution):
        self.resolution = resolution
        self.output = np.zeros([resolution, resolution, 3], dtype=np.uint8) 

    def draw(self):
        for i in range(self.resolution):
            for j in range(self.resolution):
                step_i = i/self.resolution*256
                step_j = j/self.resolution*256
                self.output[i, j] = [step_j, step_i, 255-step_j]
        
        return self.output.copy()
            
    def show(self):
        plt.axis('off')
        plt.xticks([])
        plt.yticks([])
        plt.imshow(self.output)
        plt.show()


