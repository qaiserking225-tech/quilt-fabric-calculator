# Quilt Fabric Calculator

A free quilt math calculator that answers four questions from one quilt size: quilt-top yardage, backing and batting, binding, and squares per yard.

**Live demo:** https://toolnestcalc.com/quilt-fabric-calculator/

## What it does

- **Quilt-top yardage** by the piece-count method: cut size is finished size plus 1/2 in for two 1/4 in seams, strips counted from real pieces, yardage rounded up to the next 1/8 yd, with an optional waste allowance (10 percent on top only)
- **Backing and batting** for standard and wide (108 in) backing, with both vertical and horizontal layouts computed and the smaller yardage recommended; 1/2 in seam allowance per seam; overage per side 4, 6 or 8 in
- **Binding** for straight-grain and bias (bias multiplies yardage by 1.5), with strip width, join allowance and usable width inputs
- **Squares** by grid count, never area division: squares per yard, squares per fat quarter, and yardage or fat quarters for any number of squares
- Size presets (baby through California king) plus custom dimensions, with a shared quilt size across all four sections

## Why piece-count, not area

An area shortcut (quilt area times a factor) understates yardage when pieces are small, because it ignores strip-remainder waste. This calculator counts real strips and real pieces, so it matches what you actually cut. If the quilt size is not an exact multiple of the block size, the finished quilt shrinks to the nearest multiple and the page shows that actual size.

## Use

Open `index.html` in any browser. No build step, no backend, no dependencies. Defaults: Throw 60 x 72 in, usable width 42 in, block 6 in, giving top 4 yd, backing 3 7/8 yd (horizontal), binding 1/2 yd, total 8 3/8 yd.

The core math lives in `qTop()`, `qBacking()`, `qBinding()` and `qYardsForSquares()` in `index.html`, with no dependencies. The same functions are exported for Node (`module.exports`) so the math can be unit-tested without a browser.

## Scope

Borders are not covered: border yardage with multiple borders and mitered corners is a separate calculation.

## License

MIT. See `LICENSE`.
