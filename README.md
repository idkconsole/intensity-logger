# Intensity Logger

A simple and flexible logging module with customizable intensity and color-coded output for enhanced readability.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
  - [Basic Usage](#basic-usage)
  - [Log Levels](#log-levels)
  - [Performance Timing](#performance-timing)
- [Contributing](#contributing)
- [License](#license)

## Introduction
Intensity Logger is a Python logging module designed to provide simple, color-coded logging output with customizable intensity. It helps to easily distinguish different log levels, such as debug, info, warning, error, success, and ratelimit.

## Features
- Color-coded log messages for easy readability.
- Support for different log levels: debug, info, warning, error, success, and ratelimit.
- Optional custom intensity to convert messages to uppercase.
- Lightweight and easy to integrate into any Python project.

## Installation
You can install Intensity Logger via pip:

```bash
pip install intensity-logger==0.1.1
```

## Usage
## Basic Usage

Here's a basic example to get you started with Intensity Logger:

```py
from intensity_logger import Logger

logger = Logger()

logger.debug("This is a debug message.")
logger.info("This is an info message.")
logger.warning("Warning issued.")
logger.error("An error has occurred.")
logger.success("Operation was successful.")
logger.ratelimit("Rate limit exceeded.")
```

## Log Levels
Intensity Logger supports various log levels, each with a different color:

- Debug: Detailed information, typically of interest only when diagnosing problems.
- Info: Confirmation that things are working as expected.
- Warning: An indication that something unexpected happened, or indicative of some problem in the near future.
- Error: Due to a more serious problem, the software has not been able to perform some function.
- Success: Indicates successful operations.
- Ratelimit: Warnings about rate limiting.

## Performance Timing
You can log the duration of an operation by passing `start` and `end` times:

```py
import time
from intensity_logger import Logger

logger = Logger()

start_time = time.time()
time.sleep(2)
end_time = time.time()

logger.success("Operation completed successfully.", start=start_time, end=end_time)
```

## Contributing

Contributions are welcome! If you have ideas for improvements or new features, feel free to open an issue or submit a pull request on GitHub.

1. Fork the repository.
2. Create your feature branch.
3. Commit your changes.
4. Push to the branch.
5. Open a pull request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
