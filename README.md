# SuperParental

**SuperParental** is a tool designed to manage, inspect, and modify Android APKs with the help of automation tools such as `apktool` and digital signing utilities. It leverages Node.js for orchestration and Docker for isolated builds.

## Features

- Decompile Android APKs
- Modify AndroidManifest and resources
- Rebuild and sign APKs automatically
- Docker support for reproducible builds

## Project Structure

```
SuperParental/
├── index.js                # Main entry point
├── dockerfile              # Docker configuration for build environment
├── SP_Dockerfile           # Specialized Dockerfile for SuperParental
├── app/
│   └── factory/            # APK tooling (apktool, sign tool, keys)
├── package.json            # Node.js dependencies
├── LICENSE
```

## Prerequisites

- Node.js (v14+)
- Docker (optional, for containerized operations)
- Java (for running JAR-based tools)

## Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/SuperParental.git
   cd SuperParental
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Run the tool**
   ```bash
   node index.js
   ```

## Docker Usage

Build the Docker image:
```bash
docker build -f SP_Dockerfile -t superparental .
```

Run the container:
```bash
docker run -v $(pwd):/app superparental
```

## Author

**Sumit Singh Sengar**

## License

This project is licensed under the terms of the MIT license.
