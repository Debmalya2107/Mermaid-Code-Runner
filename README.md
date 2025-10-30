#!/bin/bash

# Mermaid 3D Studio - Project Setup Script
# This script creates the complete project structure with README

# Color codes for output
RED='\033[0;31m'
GREEN='\033[0;32m'
YELLOW='\033[1;33m'
BLUE='\033[0;34m'
PURPLE='\033[0;35m'
CYAN='\033[0;36m'
NC='\033[0m' # No Color

# Function to print colored output
print_status() {
    echo -e "${GREEN}[INFO]${NC} $1"
}

print_warning() {
    echo -e "${YELLOW}[WARNING]${NC} $1"
}

print_error() {
    echo -e "${RED}[ERROR]${NC} $1"
}

print_header() {
    echo -e "${PURPLE}================================${NC}"
    echo -e "${CYAN}$1${NC}"
    echo -e "${PURPLE}================================${NC}"
}

# Create project directory
print_header "Creating Mermaid 3D Studio Project"

PROJECT_NAME="mermaid-3d-studio"
print_status "Creating project directory: $PROJECT_NAME"

mkdir -p "$PROJECT_NAME"
cd "$PROJECT_NAME" || exit 1

# Create directory structure
print_status "Creating directory structure..."
mkdir -p {assets,docs,examples,scripts}

# Create README.md file
print_status "Generating README.md..."

cat > README.md << 'EOF'
# Mermaid 3D Studio

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/version-1.0.0-green.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

A stunning, feature-rich Mermaid diagram editor with immersive 3D effects and animations. Transform your diagrams into interactive visual experiences with our modern, glass-morphism interface.

## ✨ Features

- 🎨 **3D Visual Effects**: Immersive 3D transformations, floating animations, and perspective effects
- 🔄 **Live Preview**: Real-time rendering of Mermaid diagrams as you type
- 📚 **Pre-built Examples**: Quick-start templates for various diagram types
- 🎭 **Multiple Themes**: Choose from different color schemes for your diagrams
- 💾 **Export Options**: Save your diagrams as SVG files
- 🔗 **Share Functionality**: Generate shareable links with encoded diagram data
- 📱 **Responsive Design**: Works seamlessly on desktop and mobile devices
- ⌨️ **Keyboard Shortcuts**: Productivity-boosting hotkeys
- 🌈 **Animated Backgrounds**: Dynamic gradient backgrounds with particle effects
- 🖱️ **Interactive Elements**: Mouse-tracking 3D effects and smooth transitions

## 🚀 Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- No additional dependencies required!

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/mermaid-3d-studio.git
