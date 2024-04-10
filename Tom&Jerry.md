import pygame
import sys

# Initialize Pygame
pygame.init()

# Set up the screen
WIDTH, HEIGHT = 800, 600
screen = pygame.display.set_mode((WIDTH, HEIGHT))
pygame.display.set_caption("Tom and Jerry Running")

# Load images
tom_image = pygame.image.load("tom.png")  # Make sure to replace "tom.png" with the actual image file
jerry_image = pygame.image.load("jerry.png")  # Make sure to replace "jerry.png" with the actual image file

# Set initial positions
tom_x, tom_y = 50, HEIGHT - 150
jerry_x, jerry_y = 50, HEIGHT - 100

# Set movement speed
tom_speed = 5
jerry_speed = 7

clock = pygame.time.Clock()

# Main loop
while True:
    screen.fill((255, 255, 255))  # Fill the screen with white color
    
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            pygame.quit()
            sys.exit()

    # Move Tom and Jerry
    tom_x += tom_speed
    jerry_x += jerry_speed

    # Wrap around when reaching the end of the screen
    if tom_x > WIDTH:
        tom_x = -tom_image.get_width()
    if jerry_x > WIDTH:
        jerry_x = -jerry_image.get_width()

    # Blit images to the screen
    screen.blit(tom_image, (tom_x, tom_y))
    screen.blit(jerry_image, (jerry_x, jerry_y))

    pygame.display.flip()
    clock.tick(60)  # Cap the frame rate at 60 frames per second
