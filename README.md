<h1 align="center">
    <span>Arista AI</span>
    <img height="30" src="https://pbs.twimg.com/profile_banners/1870565954180055040/1734813022/1500x500" alt="Arista logo"/>
</h1>

<p align="center">
    Transforming ideas into music with the power of AI. Experience next-gen music creation and tokenization.
</p>

<p align="center">
    <a href="https://aristalabs.org">Website</a> | <a href="https://x.com/AristaLab">Twitter</a>
</p>

# Overview

Arista is an AI-driven platform for music creation, offering innovative tools to generate music effortlessly using natural language prompts. With support for advanced models like MusicGen, Arista allows you to create, customize, and monetize music, all on a decentralized framework.

### Key Features:
- **Text-to-Music**: Create music with simple text descriptions.
- **Real-Time Generation**: Instant music creation powered by AI.
- **Style Transfer**: Apply different musical styles to your tracks.
- **Infinite Music**: Generate endless, non-repeating music streams.
- **Tokenized Music Economy**: Monetize and share your music with blockchain transparency.

# Installation

## Mac and Linux

Install Arista AI tools using `brew`:

```shell
brew install gabotechs/taps/arista
```

Or download the precompiled binaries directly from [our latest release](https://github.com/gabotechs/MusicGPT/releases/latest).

## Windows

Download the Windows executable from [this link](https://github.com/gabotechs/MusicGPT/releases/latest/download/x86_64-pc-windows-msvc.tar.gz).

## Docker (Recommended for CUDA-enabled GPUs)

For systems with CUDA-enabled GPUs, use Docker for optimal performance:

```shell
docker pull gabotechs/musicgpt
```

Run the image with:

```shell
docker run -it --gpus all -p 8642:8642 -v ~/.musicgpt:/root/.local/share/musicgpt gabotechs/musicgpt --gpu --ui-expose
```

## Using Rust Cargo

Install with the Rust toolchain:

```shell
cargo install musicgpt
```

# Usage

### UI Mode

Access Arista’s intuitive chat-like interface for generating music. This mode enables:
- Chat history for easy reference.
- Playback of generated music samples.
- Background generation for efficiency.
- Cross-device usage through web access.

Start the UI with:

```shell
arista
```

For GPU support and advanced models:

```shell
arista --gpu --model medium
```

Run with Docker for GPU optimization:

```shell
docker run -it --gpus all -p 8642:8642 -v ~/.musicgpt:/root/.local/share/musicgpt gabotechs/musicgpt --ui-expose --gpu
```

### CLI Mode

Generate music directly in the terminal with text prompts:

```shell
arista "Create a relaxing LoFi song"
```

Set the duration of the audio:

```shell
arista "Create a relaxing LoFi song" --secs 30
```

Choose different AI models for inference:

```shell
arista "Create a relaxing LoFi song" --model medium
```

Review all available options with:

```shell
arista --help
```

# Benchmarks

Performance comparison for generating 10 seconds of audio using different models on Mac M1 Pro:

<p align="center">
<img height=400 src="https://github.com/gabotechs/MusicGPT/assets/45515538/edae3c25-04e3-41c3-a2b5-c0829fa69ee3"/>
</p>

# Storage

Arista saves data (models, audio, metadata) in the following locations:

- **Windows**: `C:\Users\<username>\AppData\Roaming\gabotechs\arista`
- **MacOS**: `/Users/<username>/Library/Application\ Support/com.gabotechs.arista`
- **Linux**: `/home/<username>/.config/arista`

# License

The code is licensed under [MIT License](./LICENSE). Model weights downloaded by the application are licensed under [CC-BY-NC-4.0 License](https://spdx.org/licenses/CC-BY-NC-4.0), referencing the following repositories:

- https://huggingface.co/facebook/musicgen-small
- https://huggingface.co/facebook/musicgen-medium
- https://huggingface.co/facebook/musicgen-large
- https://huggingface.co/facebook/musicgen-melody
