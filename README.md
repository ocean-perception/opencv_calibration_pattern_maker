# OpenCV calibration pattern maker

This program generates OpenCV calibration patterns

## Usage

```
python gen_pattern.py --help
usage: gen_pattern.py [-H] [-o OUTPUT] [-c COLUMNS] [-r ROWS] [-T {circles,acircles,checkerboard}] [-u {mm,inches,px,m}] [-s SQUARE_SIZE] [-R RADIUS_RATE] [-w PAGE_WIDTH] [-h PAGE_HEIGHT]
                      [-a {A0,A1,A2,A3,A4,A5}]

generate camera-calibration pattern

options:
  -H, --help            show help
  -o OUTPUT, --output OUTPUT
                        output file
  -c COLUMNS, --columns COLUMNS
                        pattern columns
  -r ROWS, --rows ROWS  pattern rows
  -T {circles,acircles,checkerboard}, --type {circles,acircles,checkerboard}
                        type of pattern
  -u {mm,inches,px,m}, --units {mm,inches,px,m}
                        length unit
  -s SQUARE_SIZE, --square_size SQUARE_SIZE
                        size of squares in pattern
  -R RADIUS_RATE, --radius_rate RADIUS_RATE
                        circles_radius = square_size/radius_rate
  -w PAGE_WIDTH, --page_width PAGE_WIDTH
                        page width in units
  -h PAGE_HEIGHT, --page_height PAGE_HEIGHT
                        page height in units
  -a {A0,A1,A2,A3,A4,A5}, --page_size {A0,A1,A2,A3,A4,A5}
                        page size, superseded if -h and -w are set
```

## Examples
 - For Biocam: `python gen_pattern.py -o acircleboard.svg --rows 13 --columns 8 --type acircles --square_size 62.5 --radius_rate 2.5 -w 1200 -h 1000 --units mm`
 - For Smarty200: `python gen_pattern.py -o acircleboard.svg --rows 13 --columns 8 --type acircles --square_size 31.25 --radius_rate 2.5 -w 594 -h 420 --units mm`
