---

# InMemory Cache Benchmarking Demo

This repository contains a Python script for benchmarking the performance of a cache using a sample function (`llm_langchain`) as a test prompt. The script is designed to be executed on Google Colab notebooks.

## Introduction

The Cache Benchmarking Demo is a Python script that measures the execution time of a cache for a specific function (`llm_langchain`) that processes a given text. The script is designed to show the time difference between the first execution (bypassing the cache) and subsequent cache hits.

The demo utilizes the `timeit` module to calculate the execution time for each iteration. It provides valuable insights into how caching can significantly improve the performance of repetitive operations.

**Note:** Before running the demo, ensure you have an OpenAI API key. Replace `YOUR_OPENAI_API_KEY` in the script with your actual API key.

## Usage on Google Colab

1. Open Google Colab in your web browser: [https://colab.research.google.com/](https://colab.research.google.com/).

2. In Google Colab, click on "File" > "New Notebook" to create a new notebook.

3. In the code cell, paste the following to clone the repository and run the benchmarking demo:

```python
!git clone https://github.com/mrodgers/demo-testing/blob/main/InMemory_Cache_Demo.ipynb
%cd cache-benchmark-demo
!pip install openai  # Install OpenAI library
!python benchmark.py --api_key=YOUR_OPENAI_API_KEY
```

4. Replace `your_username` with your actual GitHub username and `YOUR_OPENAI_API_KEY` with your OpenAI API key.

5. Click on the "Run" button to execute the code. The benchmarking demo will run, and you will see the output showing the execution times.

## Functionality

### `llm_langchain(text)`

The `llm_langchain` function represents a sample prompt processing function. It should be implemented to perform some meaningful processing on the given text and return the result. In this demo, we have implemented a placeholder function that simply returns the input text. Replace this function with your actual prompt processing logic for accurate benchmarking.

### Benchmarking

The script performs the following steps for benchmarking the cache:

1. First Execution (Bypassing Cache):
   The script runs the `llm_langchain` function once to measure the time it takes for the first execution without utilizing the cache. This time represents the execution time without cache hits.

2. Cache Hits (Subsequent Executions):
   After the first execution, the script runs the `llm_langchain` function multiple times (`num_iterations`) to simulate cache hits. The time taken for each execution is measured, and the average execution time is calculated for cache hits.

## Contributing

Contributions to this cache benchmarking demo are welcome! If you find any issues, have suggestions, or want to extend the functionality, feel free to create a pull request.

## License

The Cache Benchmarking Demo is open-source software licensed under the [MIT License](LICENSE).

---
