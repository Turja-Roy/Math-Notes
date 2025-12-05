# Agent Guidelines for Calc-II LaTeX Notes

## Build Commands
- **Compile PDF**: `pdflatex Calc-II.tex` (run twice for TOC updates)
- **Quick check**: `pdflatex -halt-on-error Calc-II.tex`
- **Clean**: `rm -f *.aux *.log *.toc *.out`

## Project Structure
- `Calc-II.tex`: Main document with includes
- `preamble.tex`: All packages, custom environments, and macros
- `sections/*.tex`: Individual topic sections (numbered 1-6)

## Code Style Guidelines

### Custom Environments (defined in preamble.tex)
- Use `\Definition{Title}{content}` for definitions (cyan boxes)
- Use `\Theorem{Title}{content}` for theorems (green boxes, italic)
- Use `\Corollary{Title}{content}` for corollaries (green boxes, no frame)
- Use `\Example{Title}{content}` for examples (gray boxes)
- Use `\Note[Optional Title]{content}` for notes (default title: "Note:-")

### Math Conventions
- Use `\dd{x}` for differentials (from physics package)
- Use `\dv{}{x}` for derivatives, `\pdv{}{x}` for partial derivatives
- Inline math: `$...$`, display math: `\[...\]` or equation environments
- Common sets: `\R`, `\N`, `\Z`, `\Q`, `\C` (predefined macros)
- Use `\lvert` and `\rvert` for absolute values, not plain `|`

### Formatting
- Section headings with comment blocks: `%%%%%%%%%%%%%` above/below
- Use `\subsection{}` for major topics within sections
- Tables with `[htpb]` positioning and centered captions
- Line breaks: `\\~\\` for spacing between items
- Use `\begin{minipage}` for side-by-side content

### General Conventions
- Keep consistent spacing: blank line before/after environments
- Array stretch: `\renewcommand{\arraystretch}{1.5}` in main doc
- Use `\newpage` between sections in main document
- Geometric series use `a^n` notation consistently
- Always include `+ c` for indefinite integrals

## Notes
- This is a personal study notes repository for Calculus II
- No automated tests or linting
- Recent commits focus on series, sequences, and Taylor's theorem
