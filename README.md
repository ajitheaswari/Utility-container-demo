# Utility Container Demo 🚀

A demo repository showcasing how to build, package, and run utility images using Docker. It includes sample utilities wrapped as standalone containers with easy CLI usage.

---

## 📁 Repository Structure

utility-container-demo/
├── dockerfiles/
│ ├── hello-world/
│ │ ├── Dockerfile
│ │ └── entrypoint.sh
│ └── text-utils/
│ ├── Dockerfile
│ ├── entrypoint.sh
│ └── utils.py
├── scripts/
│ └── build_all.sh
├── .gitignore
└── README.md

- **`dockerfiles/`**: Contains individual utility Dockerfiles and their entry scripts.
  - `hello-world`: A basic container printing "Hello, world!"
  - `text-utils`: Contains text-processing utility script using Python.
- **`scripts/`**: Includes helper scripts such as `build_all.sh` to build all utility images at once.
- **`.gitignore`**: Standard ignores.
- **`README.md`**: This documentation file.

---

## 🧰 Utilities

1. **Hello World**
   - **Purpose**: Basic test container.
   - **Image Tag**: `utility/hello-world:latest`
   - **Usage**:
     ```bash
     docker run --rm utility/hello-world
     ```

2. **Text Utils**
   - **Purpose**: Lightweight text-processing tool (e.g., uppercase conversion).
   - **Image Tag**: `utility/text-utils:latest`
   - **Usage**:
     ```bash
     echo "hello container" | docker run --rm -i utility/text-utils
     # Output: HELLO CONTAINER
     ```

---

## 🛠️ Build Instructions

### Local Build
From repo root:
```bash
# Build individual utility
docker build -t utility/hello-world ./dockerfiles/hello-world
docker build -t utility/text-utils ./dockerfiles/text-utils

# Or build all at once:
scripts/build_all.sh
