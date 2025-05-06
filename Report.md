# SEEM3650 Practical Exam 2 babychatgpt 
nanoGPT
Descripe: Explore training GPT models using the nanoGPT repository. While
training functioning GPT models typically requires multiple GPUs, we will work with a much smaller
version, referred to as BabyGPT. This can be trained on a CPU, though using a GPU (e.g., via Google
Colab) is recommended for faster results.
SID:1155193525
Name: Leung ShingYip

# Practical Exam Report
##  Step 1 : Cloning

!git clone https://github.com/karpathy/nanoGPT

Given:Cloning into 'nanoGPT'...
remote: Enumerating objects: 686, done.
remote: Total 686 (delta 0), reused 0 (delta 0), pack-reused 686 (from 1)
Receiving objects: 100% (686/686), 954.03 KiB | 23.85 MiB/s, done.
Resolving deltas: 100% (387/387), done.

## Step 2: Shakespeare Model Output
## Shakespeare Character-level Model Samples

Overriding: out_dir = out-shakespeare-char
Overriding: max_new_tokens = 1000
number of parameters: 10.65M
Loading meta from data/shakespeare_char/meta.pkl...


**First 5 lines outputs:**
AUTOLYCUs: O, will you be straightMENENlUS: Stirrd your gates?
CORIOLANUS: You met?MENENlUs: Nay, no more not to be much:lf you find it out of much but soils, since l lay you, i'l speak with her person of else no moreAUFiDlUs: l would have show'd your name. Be patient o'er the world that Would so what evil so you would have no precise of mine; Which
you have forgot a sign of sheet in all of person The ground.

## Step 3: Structure Exploration validation loss vs layer depth

