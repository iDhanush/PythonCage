# PythonCage

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/Version-1.0.0-green.svg)](https://github.com/yourusername/PythonCage/releases/tag/v1.0.0)

PythonCage is a powerful Python library designed to execute Python code within predefined restrictions and limits. It provides a secure and controlled environment for running potentially untrusted code, ensuring that it operates within specified resource boundaries. If these boundaries are exceeded, PythonCage automatically restarts the Python program, preventing any potential harm.

## Features

- **Resource Limits**: Define limits on CPU usage, memory consumption, execution time, and other system resources to prevent abuse or excessive resource utilization.

- **Automatic Restart**: PythonCage monitors the execution of the Python code, and if it detects that the specified restrictions or limits are exceeded, it gracefully restarts the Python program.

- **Isolated Execution**: Run untrusted code in an isolated environment, protecting your system from potential security threats.

- **Customizable Configuration**: Fine-tune PythonCage to fit your specific needs by configuring resource limits and restart behavior according to your application's requirements.

## Installation

You can install PythonCage using `pip`:

```bash
pip install PythonCage
```
Usage

```bash
from PythonCage import PythonCage

# Create a PythonCage instance with specified limits
cage = PythonCage(cpu_limit=1, memory_limit=512)  # 1 second CPU limit, 512 MB memory limit

# Execute Python code within the cage
code = """
print("Hello, PythonCage!")
"""

cage.execute(code)
```
