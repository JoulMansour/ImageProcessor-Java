# ImageProcessor-Java (ASCII Art Generator)

A Java program that converts an input image into **ASCII art** using brightness matching.
It includes an interactive shell where you can control **resolution**, **charset**, **output mode** (console/HTML), and **brightness reversal**.

## How it works (high level)
- Loads an image from disk using `ImageIO`. :contentReference[oaicite:4]{index=4}
- Pads the image to the nearest **power-of-two** dimensions (with white pixels), then splits it into sub-images according to the chosen resolution.
- Computes each sub-image brightness using a weighted grayscale formula and maps brightness to the closest character in the active charset. 
- Can cache brightness calculations for the same image+resolution to speed up repeated runs.


## How to Run
1. Clone this repository.
2. Open the project in your preferred Java IDE (e.g., IntelliJ IDEA, Eclipse).
3. Run the `main` method located in `ascii_art.Shell`.
4. When prompted / or as an argument (depending on your IDE run configuration), provide a path to an image file.

