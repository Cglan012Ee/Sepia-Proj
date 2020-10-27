# Sepia-Proj
import turtle



def grayscale(image):
    for y in range(image.getHeight()):
        for x in range(image.getWidth()):
            (r, g, b) = image.getPixel(x, y)
            r = int(r * 0.299)
            g = int(g * 0.587)
            b = int(b * 0.114)
            lum = r + g + b
            image.setPixel(x, y, (lum, lum, lum))

def main():
    screen = turtle.Screen()
    screen.setup(500,500)
    image = "sunflower.gif"

    t = turtle.Turtle()

    screen.addshape("sunflower.gif")
    t.shape("sunflower.gif")
    grayscale(image)

if __name__ == "__main__":           

    main()
