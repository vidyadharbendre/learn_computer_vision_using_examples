# Shannon’s Sampling Theorem and Nyquist Frequency

## Minimum Sampling Rate

Shannon’s Sampling Theorem states that the minimum sampling rate required to reconstruct a signal from its instantaneous samples must be at least twice the highest frequency:

' 
f_s ≥ 2f_{max} 
'

Here, the maximum frequency in a signal is known as the **Nyquist frequency**, and the inverse of the minimum sampling frequency 'r_s = 1/f_s' is termed the **Nyquist rate**.

## Implications for Imaging Chips

Even when an imaging chip averages the light field over a finite area, the results from point sampling remain applicable. Frequencies above the Nyquist limit (half the sampling frequency) can still produce an aliased signal, even with a 100% fill factor.

---

## References

- Szeliski, Richard. *Computer Vision: Algorithms and Applications* (Texts in Computer Science). Springer International Publishing.
