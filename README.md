Here is the content for the `README.md` file for the Parking Space Counter project:

---

# Parking Space Counter

This project is a parking space counter system that uses OpenCV to detect and count available parking spaces in a video feed. It utilizes Python with computer vision techniques to process the video, detect parking spots, and count the available spots based on empty or filled spaces.

## Project Structure

- **ParkingSpacePicker.py**: This script is used to manually define parking spaces on an image by clicking with the mouse. It saves the parking spot positions into a file using Python's `pickle` module.
- **main.py**: The main parking space detection script. It processes the video feed, checks the parking spaces, and displays the available spots on the screen with colored rectangles (green for free, red for occupied).
- **main.py (with Trackbars)**: An advanced version of the `main.py` script that includes trackbars to fine-tune thresholding values in real-time for better performance in detecting occupied and free spaces.

## How It Works

1. **Parking Space Selection**:  
   - Use the `ParkingSpacePicker.py` to mark the parking spaces on a given image.
   - Left-click to add a new parking spot.
   - Right-click to remove an existing spot.
   - The positions of the parking spots are stored in a file (`CarParkPos`) for later use.

2. **Parking Space Detection**:  
   - The video feed is processed frame by frame in `main.py`.
   - The defined parking spaces are checked by extracting each space and analyzing it using image processing techniques like blurring, thresholding, and dilation.
   - Based on the pixel count, the script determines whether the space is occupied or free and updates the display accordingly.

3. **Advanced Tuning**:  
   - The version with trackbars allows you to adjust the thresholding parameters dynamically to fine-tune the detection.

## Setup Instructions

1. Clone the repository and install the required dependencies:
   ```bash
   git clone <repo_url>
   cd ParkingSpaceCounter
   pip install -r requirements.txt
   ```

2. Run `ParkingSpacePicker.py` to manually mark the parking spots:
   ```bash
   python ParkingSpacePicker.py
   ```

3. Run `main.py` or `main.py (with Trackbars)` to start the parking space counter:
   ```bash
   python main.py
   ```

4. Optionally, use the version with trackbars for real-time tuning:
   ```bash
   python main.py --trackbars
   ```

## Dependencies

- OpenCV
- cvzone
- numpy
- pickle

Install the dependencies with:
```bash
pip install opencv-python cvzone numpy
```

## Files

- **ParkingSpacePicker.py**: Script for selecting parking spaces.
- **main.py**: Main script for parking space detection.
- **main.py (with Trackbars)**: Enhanced script with real-time adjustment via trackbars.

## Customization

- You can modify the size of the parking space rectangles by changing the `width` and `height` variables in the code.
- Adjust the thresholding values in `main.py (with Trackbars)` to improve detection performance under different lighting conditions.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---
 
