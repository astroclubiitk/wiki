---
title: Magnitudes
layout: default
parent: Night Sky
grand_parent: Observation
nav_order: 1
---

## Magnitudes

<br />
Magnitude is essentially a measure of the brightness of an object. It doesn't have any units of measurement. The lower the magnitude, the brighter the object. The magnitude scale is logarithmic in nature, i.e., a difference of 1 magnitude corresponds to a difference of ~2.5 times in brightness.

The scale was originally invented by the Alexandrian astronomer, Ptolemy, where he classified the objects on a six-point scale. In the northern hemisphere, Vega is one of the brightest stars, earning itself a magnitude of 0. The other stars were classified with Vega as reference.

More recently, the modern logarithmic magnitude scale was adopted and the Sun was placed at an [apparent magnitude](#apparent-magnitude) of approximately -27. The rest of the celestial bodies (and satellites like the ISS) followed suit.

### Apparent Magnitude

Apparent magnitude is the most widely used type of magnitude. If you have a reference object, whose magnitude is fixed (or known), the magnitude of any other object can be very easily calculated using the following formula:

$$
\begin{equation}
  m_1 - m_{ref} = -2.5 \log_{10} \left( \frac{F_1}{F_{ref}} \right)
\end{equation}
$$

where:

- $$m_1$$ = Apparent magnitude of the object you're interested in
- $$F_1$$ = Flux from the object you're interested in
- $$m_{ref}$$ = Apparent magnitude of the reference object
- $$F_{ref}$$ = Flux from the reference object

Note that the flux referred to here is generally known as intensity in physics, which can be measured in units such as watts per square metre ($$Wm^{-2}$$). You can find the apparent magnitude of some of the popular objects, arranged in decreasing order, in the following table:

| Object             | Apparent Magnitude |
| ------------------ | ------------------ |
| Sun                | -26.832            |
| Full Moon          | -12.90             |
| Venus              | -4.14              |
| Jupiter            | -2.20              |
| Sirius             | -1.46              |
| Canopus            | -0.72              |
| Arcturus           | -0.04              |
| Vega               | +0.03              |
| Saturn             | +0.46              |
| Betelgeuse         | +0.58              |
| Mars               | +0.71              |
| Altair             | +0.77              |
| Deneb              | +1.25              |
| Polaris            | +1.98              |
| Andromeda (M31)    | +3.44              |
| Orion Nebula (M42) | +4                 |

{: .fun }

> Objects with apparent magnitude less than
>
> - -4 are visibile when the Sun is high, and can cast shadows at night
> - +4.5 are visible from IIT Kanpur with naked eye
> - +7 can be captured using the [Observatory](https://astroclubiitk.github.io/resources/observatory) at IIT Kanpur
> - +34 are observable in the visible light by the JWST
>
> Rumor has it that Naveen can see objects with apparent magnitude less than 10

### Absolte Magnitude

It is a well-known theorum in physics that the intensity is inversely proportional to distance squared. Hence, one can calculate the absolute magnitude of any object if the [apparent magnitude](#apparent-magnitude) and the distance of the object from the observer is known using the following formula:

$$
\begin{equation}
  m - M = 2.5 \log_{10} (d/10)^2 = 5 (\log_{10}d - 1)
\end{equation}
$$

where:

- $$M$$ = Absolute magnitude of the object you're interested in
- $$m$$ = Apparent magnitude of the object you're interested in
- $$d$$ = Distance of the object you're interested in from you
