# TeX Live Environment

This image contains TeX Live installed from CTAN source with full scheme.

Inspired by [TinyTeX](https://yihui.org/tinytex/),  source files and documentation of packages are excluded, which reduce the size a little.



- Why is full scheme chosen?
    To ensure the compatibility. With full scheme, you can compile your colleague's source file easily at most time. In my opinion, the space for most packages deserve the time saved from debugging.

    
    
- Why is this image Debian instead of Alpine based?
    To enable Asymptote. Asymptote seems doesn't support musl libc, which is used by Alpine.

