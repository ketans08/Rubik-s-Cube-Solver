# Rubik's Cube Solver

A modern web-based application for solving Rubik's Cube puzzles using algorithmic solving techniques. This project provides an interactive interface to visualize a 3D Rubik's Cube, input the current state, and get step-by-step solutions.

## Project Structure

```
Rubiks-Cube-Solver/
├── cuber/                          # Main React application
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   │   ├── face_set/          # Cube face display and configuration
│   │   │   ├── positioning/       # 3D positioning logic
│   │   │   ├── solver/            # Solving algorithm implementation
│   │   │   └── start_page/        # Initial UI landing page
│   │   ├── App.jsx                # Main application component
│   │   ├── App.css
│   │   ├── index.css
│   │   └── main.jsx
│   ├── index.html
│   ├── vite.config.js
│   └── package.json
│
└── solver-asset/                   # Solver assets and utilities
    ├── app/                       # Main solver application
    ├── color-track-test/          # Color tracking test utilities
    └── cube/                      # Cube 3D visualization assets
```

## Features

- **Interactive 3D Cube Visualization**: View and manipulate a 3D representation of the Rubik's Cube
- **Color Input System**: Input the current state of your cube by selecting colors for each face
- **Automated Solving**: Get algorithmic solutions to solve any Rubik's Cube configuration
- **Step-by-Step Instructions**: View the solving process with clear, sequential instructions
- **Visual Feedback**: Real-time cube state updates and celebration animation upon completion

## Technology Stack

- **Frontend**: React 18.2.0
- **Build Tool**: Vite 4.0.0
- **3D Visualization**: WebGL/Three.js (via solver assets)
- **Solver Algorithm**: rubiks-cube-solver library v1.2.0
- **Styling**: CSS with custom animations
- **Effects**: react-confetti for celebration animations

## Installation

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn

### Setup

1. Clone the repository:

```bash
git clone <repository-url>
cd Rubiks-Cube-Solver
```

2. Navigate to the main application:

```bash
cd cuber
```

3. Install dependencies:

```bash
npm install
```

## Running the Application

### Development Mode

Start the development server:

```bash
npm run dev
```

The application will be available at `http://localhost:5173`

### Build for Production

Create an optimized production build:

```bash
npm run build
```

### Preview Production Build

Preview the production build locally:

```bash
npm run preview
```

## How to Use

1. **Start Page**: Begin with the interactive start page to familiarize yourself with the cube
2. **Input Your Cube**: Navigate to the Face Set component to input the current colors of your cube
   - Each face has 9 squares (3x3 grid)
   - Select the appropriate color for each square
3. **Position Configuration**: Use the positioning component to verify your cube state
4. **Solve**: Click the solve button to generate the solution
5. **View Results**: Follow the step-by-step instructions to solve your physical cube

## Project Components

### FaceSet Component

Displays and allows configuration of the six faces of the Rubik's Cube with color selection for each square.

### Positioning Component

Handles the 3D positioning and orientation of the cube visualization.

### Solver Component

Implements the solving algorithm using the `rubiks-cube-solver` library to generate move sequences.

### Start Page Component

Provides an introductory interface and tutorial for first-time users.

## Cube State Format

The cube is represented internally with six faces, each containing 9 color values:

- **Front**: Green
- **Right**: Red
- **Upper**: White
- **Down**: Yellow
- **Left**: Orange
- **Back**: Blue

## Dependencies

See [package.json](cuber/package.json) for complete dependency list.

Key packages:

- `react` & `react-dom`: UI framework
- `rubiks-cube-solver`: Core solving algorithm
- `react-confetti`: Celebration effect on successful solve
- `vite`: Build tool and dev server

## Development

### Project Scripts

- `npm run dev` - Start development server with hot module reload
- `npm run build` - Create production-ready build
- `npm run preview` - Preview production build locally

### Adding New Features

When adding new components:

1. Create a new folder in `src/components/`
2. Include `index.jsx` for the main component
3. Add `style.css` or use existing CSS modules
4. Import and integrate into `App.jsx`

## Browser Compatibility

The application works best on modern browsers that support:

- ES6+ JavaScript
- WebGL
- CSS Grid and Flexbox

## Future Enhancements

- [ ] Multiple solving algorithms with difficulty selection
- [ ] Offline support with service workers
- [ ] Timer and speedcubing features
- [ ] Solution statistics and history
- [ ] Mobile app version with touch controls
- [ ] Dark mode support

## License

[Add your license information here]

## Contributing

[Add contribution guidelines here]

## Support

For issues, questions, or suggestions, please open an issue in the repository.

---

**Happy Cubing! 🎲**
