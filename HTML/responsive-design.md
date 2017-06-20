Modern technology allows users to browse the Internet via multiple devices, such as desktop monitors, mobile phones, tablets, and more. Devices of different screen sizes, however, pose a problem for web developers: how can we ensure that a website is readable and visually appealing across all devices, regardless of screen size?

The answer: *responsive design*! 

# Pixels
Pixels are used to size content to exact dimensions. For example, if you want a div to be exactly 500 pixels wide and 100 pixels tall, then the unit of ```px``` can be used. Pixels, however, are fixed, **hard coded** values meaning that they cannot be altered without modifying the program. When a screen size changes (like switching from landscape to portrait view on a phone), elements sized with pixels can appear too small, overflow the screen, or become completely illegible.

With CSS, you can avoid hard coded measurements and use *relative measurements* instead. Relative measurements offer an advantage over hard coded measurements, as they allow for the proportions of a website to remain intact regardless of screen size or layout.

# Em
Incorporating relative sizing starts by using units other than pixels. One unit of measurement you can use in CSS to create relatively-sized content is the ```em```, written as ```em``` in CSS.

The ```em``` represents the size of the base font being used. For example, if the base font of a browser is 16 pixels (which is normally the default size of text in a browser), then 1 ```em``` is equal to 16 pixels. 2 ```em```s would equal 32 pixels, and so on. If you're interested in sizing elements in comparison to other elements nearby, then the em unit would be better suited for the job.

--example:
```
.splash-section {
  font-size: 18px;
}

.splash-section h1 {
  font-size: 1.5em;
}
```

The example above shows how to use ```em```s without relying on the default font size of the browser. Instead, a base font size (18px) is defined for all text within the ```splash-section``` element. The second CSS rule will set the font size of all ```h1``` elements inside of ```splash-section``` relative to the base font of ```splash-section``` (18 pixels). The resulting font size of ```h1``` elements will be 27 pixels.

# Rem (Root em)
The second relative unit of measurement in CSS is the *rem*, coded as ```rem```. Rem stands for *root em*. It acts similar to em, but instead of checking parent elements to size font, it checks the root element. The root element is the ```<html>``` tag. Most browsers set the font size of ```<html>``` to 16 pixels, so by default rem measurements will be compared to that value. To set a different font size for the root element, you can add a CSS rule. One advantage of using rems is that all elements are compared to the same font size value, making it easy to predict how large or small font will appear. If you are interested in sizing elements consistently across an entire website, the rem measurement is the best unit for the job. 
