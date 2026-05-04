# Puzzle

Visualization of Rubik's cube solving methods for arbitrary integer order cubes.

This project provides a visualization demonstration of Rubik's cube solving methods for arbitrary integer order cubes (2x2, 3x3, 4x4, etc.) using Python and HTML.

## Features

- Simulate Rubik's cubes of any size
- Apply solving algorithms (formulas)
- Visualize the cube state
- Interactive HTML demo
- Save cube states to SQLite database

## Installation

For Python version:

```bash
pip install -r requirements.txt
```

## Usage

### Python Version

Run the main script:

```bash
python main.py [size]
```

For example:

```bash
python main.py 3  # for 3x3
python main.py 4  # for 4x4
```

This will generate PNG images of the cube at different stages and save the states to `rubiks_cube.db`.

### Database

The script automatically creates an SQLite database `rubiks_cube.db` and saves cube states with descriptions. You can query the database to retrieve saved states.

Example query:

```sql
SELECT * FROM cube_states WHERE size = 3;
```

To view the database:

```bash
sqlite3 rubiks_cube.db "SELECT id, size, description, timestamp FROM cube_states;"
```

### HTML Version

Open `index.html` in a web browser for an interactive demo.

You can change the cube size, apply moves, scramble, and see a simple solve demo.

All basic moves (R, L, U, D, F, B with inverses) are now fully implemented.

## Files

- `main.py`: Python script for cube simulation and visualization
- `index.html`: Interactive HTML demo
- `requirements.txt`: Python dependencies
- `README.md`: This file
- `.gitignore`: Excludes generated files from version control

### HTML Version

Open `index.html` in a web browser for an interactive demo.

You can change the cube size, apply moves, scramble, and see a simple solve demo.

## Files

- `main.py`: Python script for cube simulation and visualization
- `index.html`: Interactive HTML demo
- `requirements.txt`: Python dependencies
- `README.md`: This file
