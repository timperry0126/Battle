#Developed by: Timothy Perry
import pygame

SCREEN_HEIGHT = 500
SCREEN_WIDTH = 700

class Hero():
        #Constructor
    def __init__(self,pic,h,w):
        self.option = pic
        self.image = pygame.image.load(pic + " 1.png").convert()
        self.image.set_colorkey((255,255,255))
        self.direction = 1 #1:right, 2:left, 3:up, 4:down
        self.height, self.width = h, w #picture height and width
        self.xPos, self.yPos = 1, 1 # Starting position
    
        #Deals with each input for player
    def handleKeys(self, velocity, surface):
        keys = pygame.key.get_pressed()
        
        if (keys[pygame.K_RIGHT] and self.xPos < SCREEN_WIDTH - self.width): #Moves character to the right
            self.xPos += velocity
            self.direction = 1
        if (keys[pygame.K_LEFT] and self.xPos > 0): #Moves character to the left
            self.xPos -= velocity
            self.direction = 2
        if (keys[pygame.K_UP] and self.yPos > 0): #Moves character up
            self.yPos -= velocity
            self.direction = 3
        if (keys[pygame.K_DOWN] and self.yPos < SCREEN_HEIGHT - self.height): #Moves character down
            self.yPos += velocity
            self.direction = 4

        #Prints character to screen
    def draw(self, surface):
        surface.blit(self.image, (self.xPos,self.yPos))

        #Updates player picture with coordinated picture
    def update(self):
        if(self.direction == 1):    #displays player facing right
            self.image = pygame.image.load(self.option + "2.png").convert()
            self.image.set_colorkey((255,255,255))    
        elif(self.direction == 2):  #displays player facing left
            self.image = pygame.image.load(self.option + "4.png").convert()
            self.image.set_colorkey((255,255,255))
        elif(self.direction == 3):  #displays player facing up
            self.image = pygame.image.load(self.option + "3.png").convert()
            self.image.set_colorkey((255,255,255))
        elif(self.direction == 4):  #displays player facing down
            self.image = pygame.image.load(self.option + "1.png").convert()
            self.image.set_colorkey((255,255,255))

class Enemy():
    
    def __init__(self, pic, h, w):
        self.option = pic
        self.image = pygame.image.load(pic + "1.png").convert()
        self.image.set_colorkey((255,255,255))
        self.direction = 1 #1:right, 2:left, 3:up, 4:down
        self.height, self.width = h, w #picture height and width
        self.xPos, self.yPos = 200, 200 # Starting position
        
    def ai(self):
        print("get to work")
        #Check where player is
        
        #make step towards enemy
        
        #is enemy within range

        #attack enemy
        
    def draw(self, surface):
        surface.blit(self.image, (self.xPos, self.yPos))
        
    def update(self):
        print("get to work")
