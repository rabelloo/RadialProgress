# RadialProgress
CSS pattern design for Radial Progress Bars<br>

// Built upon <a href="https://medium.com/@andsens/radial-progress-indicator-using-css-a917b80c43f9#.r64rxiy28">Anders Ingemann's great article</a>

## Usage

```HTML
<div class="radial-progress" data-progress="75">
  <div class="slice">
    <div class="fill"></div>
  </div>
  <div class="slice">
    <div class="fill"></div>
    <div class="fill fix"></div>
  </div>
  <div class="display">
    <div class="percentage">
      <div class="numbers">
        <span>-</span>
        <span>0%</span><span>1%</span><span>2%</span><span>3%</span>
        <span>4%</span><span>5%</span><span>6%</span><span>7%</span>
        <span>8%</span><span>9%</span><span>10%</span><span>11%</span>
        <span>12%</span><span>13%</span><span>14%</span><span>15%</span>
        <span>16%</span><span>17%</span><span>18%</span><span>19%</span>
        <span>20%</span><span>21%</span><span>22%</span><span>23%</span>
        <span>24%</span><span>25%</span><span>26%</span><span>27%</span>
        <span>28%</span><span>29%</span><span>30%</span><span>31%</span>
        <span>32%</span><span>33%</span><span>34%</span><span>35%</span>
        <span>36%</span><span>37%</span><span>38%</span><span>39%</span>
        <span>40%</span><span>41%</span><span>42%</span><span>43%</span>
        <span>44%</span><span>45%</span><span>46%</span><span>47%</span>
        <span>48%</span><span>49%</span><span>50%</span><span>51%</span>
        <span>52%</span><span>53%</span><span>54%</span><span>55%</span>
        <span>56%</span><span>57%</span><span>58%</span><span>59%</span>
        <span>60%</span><span>61%</span><span>62%</span><span>63%</span>
        <span>64%</span><span>65%</span><span>66%</span><span>67%</span>
        <span>68%</span><span>69%</span><span>70%</span><span>71%</span>
        <span>72%</span><span>73%</span><span>74%</span><span>75%</span>
        <span>76%</span><span>77%</span><span>78%</span><span>79%</span>
        <span>80%</span><span>81%</span><span>82%</span><span>83%</span>
        <span>84%</span><span>85%</span><span>86%</span><span>87%</span>
        <span>88%</span><span>89%</span><span>90%</span><span>91%</span>
        <span>92%</span><span>93%</span><span>94%</span><span>95%</span>
        <span>96%</span><span>97%</span><span>98%</span><span>99%</span>
        <span>100%</span>
      </div>
    </div>
  </div>
</div>
```

Unfortunately all the spans are required for the "scrolling numbers" effect. You can <a href="https://medium.com/@andsens/radial-progress-indicator-using-css-a917b80c43f9#.r64rxiy28">read more about the reasons</a>

## Options

All options are, well, optional

| Option | Element | Type | Values | Description |
| --- | --- | --- | --- | --- |
| Size | `.radial-progress` |  `class` | `xs`, `sm`, `lg` | Add one of the optional classes to the element to change its size |
| Style | `.radial-progress` | `class` | `inset`, `pie` | Add one of the optional classes to the element to change its style |
| Progress | `.radial-progress` | `attribute [data-progress]` | `0 to 100` | The number between 0 and 100 on the element's attribute will define it's percentage filled. Default is 0 |
| Color | `.fill` |  `class` or `style` | valid `background-color` values | Add your own styles to the element, either by `inline-style`, `class-styles` or `class-definition` to change its color |
| Text Color | `.numbers` | `class` or `style` | valid `color` values | Add your own styles to the element, either by `inline-style`, `class-styles` or `class-definition` to change its text color |

## Examples:

**Color + Text Color (Inline-style) + Size + Progress:**
```HTML
<div class="radial-progress xs" data-progress="50">
  <div class="slice">
    <div class="fill" style="background-color: red;"></div>
  </div>
  ...
  <div class="display">
    <div class="percentage">
      <div class="numbers" style="color: red;">
        ...
      </div>
    </div>
  </div>
</div>
```

**Color + Text Color (Class-style) + Size + Style:**
```HTML
<style>
  .fill {
    background-color: red;
  }
  .numbers {
    color: red;
  }
</style>

<div class="radial-progress sm pie">
  <div class="slice">
    <div class="fill"></div>
  </div>
  ...
  <div class="display">
    <div class="percentage">
      <div class="numbers">
        ...
      </div>
    </div>
  </div>
</div>
```

**Color + Text Color (Class-definition) + Size + Style:**
```HTML
<style>
  .red {
    background-color: red;
  }
  .text-red {
    color: red;
  }
</style>

<div class="radial-progress lg inset">
  <div class="slice">
    <div class="fill red"></div>
  </div>
  ...
  <div class="display">
    <div class="percentage">
      <div class="numbers text-red">
        ...
      </div>
    </div>
  </div>
</div>
```

**You can also:**

- Replace `.numbers` with your markup of choice. You can show centered text this way.
- Replace `.percentage` with your markup of choice. You can use the whole Radial Progress Bar center area this way.
- Replace `.numbers`'s `<span>`'s values to animate other values or text. Keep in mind the `data-progress` still only goes from 0 to 100.
- Use JavaScript to animate the percentage numbers in `.numbers` and cut off all the `<span>`s, both in `HTML` and `CSS`.
