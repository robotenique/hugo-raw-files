---
title:  "Atom & Latex"
linktitle:  "Atom & Latex"
date:   2017-05-24
categories: ["Misc"]
tags: ["programming", "environment"]

---

LaTeX is a DSL (*domain specific language*) that provides powerful typesetting tools. You can write complex mathematical expressions and much more, for example, the following characteristic polynomial expression was rendered using LaTeX (MathJax):

[//]: # (In Hugo you need to use SIX backlashes to linebreak)

$$  \chi(\lambda) = \left| \begin{array}{ccc}
\lambda - a & -b & -c \\\\\\
-d & \lambda - e & -f \\\\\\
-g & -h & \lambda - i \end{array} \right|  $$

There are amazing online software to work with LaTeX such as [ShareLaTeX](https://www.sharelatex.com/) or [Overleaf](https://www.overleaf.com/), but sometimes you don't have access to the internet, or want to have a compact environment to do most of your job. This is a simple tutorial about how to configure the [Atom Editor](/misc/2017/03/21/atom-edit.html) to work with LaTeX.

{{< image
    src="/img/atom-latex.png"
    alt="atom-latex" >}}

## How to install

I'm assuming you have Atom installed and know how to install plugins in Atom.

### **1.TeX distribution**

To use packages and the full power of LaTeX, I recommend the TeXLive. TeXLive comes with a LOT of packages and utility for LaTeX. The size of the installation is big ( > 800 MB), but you'll have almost everything you need in LaTeX, and is very easy to install.

The two commands below will install the complete packages that I use, plus a few extra ones (very recommended!).

~~~bash
$ sudo apt-get install texlive
$ sudo apt-get install texlive-latex-extra
~~~

### **2.Install compilers for LaTeX**

The Atom plugin depends on some compilers to parse the  *.tex* files, so we need to install them too. This is a very important step that most people forget and then just blame the plugins...

We'll install the **texify**, which is a compilation driver, and **latexmk** to automate the process of generating LaTeX documents.

~~~bash
$ sudo apt-get install texify
$ sudo apt-get install latexmk
~~~

### **3.Atom plugins**

Finally, we'll install the Plugins. You can use LaTeX in Atom with a variety of plugins, here I'll cover the ones that I use.

- [language-latex](https://atom.io/packages/language-latex)
    Add syntax highlighting for *.tex* in Atom, optional but **very** recommended!

- [pdf-view](https://atom.io/packages/pdf-view)
    This neat plugin enables PDF display in Atom, and is used by the next plugin to show your compiled LaTeX file;

- [latextools](https://atom.io/packages/latextools)
    This is the most important plugin, as it allows you to compile your .tex file using CTRL + ALT + B.

If everything was correctly installed, *latextools* will work fine as expected, and that's it!
