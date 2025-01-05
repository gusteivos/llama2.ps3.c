# llama2.ps3.c

TODO.

---

## Inspired By

This project was inspired by [this post](https://x.com/AndreiDavid/status/1874079931958956364).

---

## Based On

The implementation is based on the work available in [karpathy/llama2.c](https://github.com/karpathy/llama2.c).

---

## Compiling

For the build process, you will need to install [ps3toolchain](https://github.com/ps3dev/ps3toolchain). Make sure it works on your system before proceeding.

After that, it will be necessary to clone [karpathy/llama2.c](https://github.com/karpathy/llama2.c):

```bash
git clone https://github.com/karpathy/llama2.c
```

Download a Llama2 model checkpoint. For example:

```bash
wget https://huggingface.co/karpathy/tinyllamas/resolve/main/stories15M.bin -O model.bin
```

Then, clone this repository:

```bash
git clone https://github.com/gusteivos/llama2.ps3.c.git
```

Copy the required files into the `llama2.ps3.c` repository:

```bash
cp llama2.c/tokenizer.bin llama2.ps3.c/data/
cp model.bin llama2.ps3.c/data/
```

Navigate to the repository folder:

```bash
cd llama2.ps3.c/
```

Before using `make` to compile the main project, compile and install some modifications made to the PS3 SDK:

```bash
make -C psl1ght/ all
```

Now, compile the main project:

```bash
make
```

---

## Running

The simplest way to run this project is to use RPCS3. Install and configure it by following the instructions available [here](https://github.com/RPCS3/rpcs3).

Once RPCS3 is set up, run the compiled project using:

```bash
rpcs3 ./llama2.ps3.c.self
```
