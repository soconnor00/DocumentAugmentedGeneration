# Document Augmented Generation

This is a fork of https://github.com/afaqueumer/DocQA focused on the document augmented generation aspect of the project.

# Requirements

- Python 3.9
- .gguf files for your chosen Llama version, I used the ones here: https://huggingface.co/TheBloke/Llama-2-7B-GGUF. He also has versions for the 13B and 70B models.
    * Update the file paths in the notebooks to match your chosen model name

## Windows Requirements

I do not recommend trying to get this project working on Windows, but if you must, here are some extra requirements:

- Visual Studio Build Tools
- CUDA Toolkit (or AMD equivalent, although I haven't tested it)
- Run these commands after installing the above:
```
set CMAKE_ARGS=-DLLAMA_CUBLAS=on
set FORCE_CMAKE=1
pip install llama-cpp-python
```
- Before running scripts, move them all out of the `scripts` directory up one level, and update the paths in the notebooks accordingly. Some of the libraries used don't like having to traverse up the file directory.

There may be other requirements for your box, but the above are the ones I had to install.

# Setup

```
pip install -r requirements.txt
```
or
```
pipenv install
```

Expect to encounter problems I haven't listed here. Running LLMs tends to be a very hardware-specific problem, but the setup is by far the hardest part here.

## Contributing
Contributions to this app are welcome! If you have any ideas, suggestions, or bug fixes, please feel free to open an issue or submit a pull request. We appreciate your contributions.

## License
This project is licensed under the MIT License.

