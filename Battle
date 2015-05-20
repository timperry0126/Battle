#Developed by: Timothy Perry

import os
import pygame
from Character import *

WHITE = (255,255,255)
BLACK = (0,0,0)

def main():

    pygame.init()
    pygame.font.init()
    pygame.mixer.init()

    screenWidth = 700
    screenHeight = 500

    size = (screenWidth, screenHeight)
    screen = pygame.display.set_mode(size)
    pygame.display.set_caption("Battle Time")

    done = False

    clock = pygame.time.Clock() 
    hero = Hero("Arrow_", 20, 20)   #Creation of player
    enemy = Enemy("Arrow_", 20, 20)
    velocity = 2    #Controls how fast character moves

    levelSelector = 1   #Chooses what level to play

    field = pygame.image.load("Sand.png")
    
    myfont = pygame.font.SysFont("monospace", 100)
    label = myfont.render("Battle!", 1, (BLACK))
    myfont2 = pygame.font.SysFont("monospace", 30)
    label2 = myfont2.render("Press Enter to Start", 1, (BLACK))

        #Game loop begins
    while not done:

        for event in pygame.event.get():
            if(event.type == pygame.QUIT):
                pygame.quit()
                done = True
        #--- Title Screen -----------------------

        if(levelSelector == 1):

            screen.fill(WHITE)
            screen.blit(label,(150,110))
            screen.blit(label2, (170,250))

            keys = pygame.key.get_pressed()

            if(keys[pygame.K_RETURN]):
                levelSelector = 2
            
            pygame.display.flip()
            
        #--- Battle Screen ----------------------

        if(levelSelector == 2):

            screen.fill(WHITE)
            screen.blit(field, (0,0))
            hero.update()
            
            hero.draw(screen)
            enemy.draw(screen)
            
            hero.handleKeys(velocity, screen)

            pygame.display.flip()
            
            clock.tick(60)

main()
    
