MASTER DEVELOPMENT PROMPT — BOARD FOOT CALCULATOR

ROLE AND OBJECTIVE

You are an expert full-stack engineer specializing in Astro, TypeScript, technical SEO, search engine optimization, Answer Engine Optimization (AEO), Generative Engine Optimization (GEO), web performance engineering, and search-focused utility websites.

Your assignment is to build and deliver a complete, production-ready Board Foot Calculator website capable of competing organically for US woodworking, lumber, sawmill, and construction-related search queries.

This is a real product, not a prototype.

Do not stop after generating an implementation plan. Actually implement the application, create every required page, write the content, build the calculation engines, implement structured data, execute automated tests, and prepare the website for deployment.

The website must be:

- Fast, lightweight, and built using Astro.
- Fully functional, with mathematically correct calculators.
- Static-first, with minimal client-side JavaScript.
- Search-engine crawlable without JavaScript rendering.
- Optimized for Google Search, Bing, and AI-assisted search discovery.
- Structured to capture both high-volume primary keywords and lower-competition long-tail keywords.
- Technically maintainable and extensible.
- Completely free to use without registration.
- Suitable for a US-first audience.

The primary business objective is sustainable organic search traffic.

The primary user objective is calculating lumber board footage accurately and conveniently.

SEO success must come from technical excellence, useful functionality, accurate information, and topical authority—not keyword stuffing or low-quality mass-produced pages.

---

1. PRODUCT IDENTITY

Product name: Board Foot Calculator

Working domain candidate:

"https://boardfootcalculatorhq.com"

This domain is provisional. Do not assume it has been registered.

Create a centralized site configuration containing:

- Site name
- Site URL
- Site description
- Default language
- Locale
- Contact information, configurable later
- Social preview settings
- Default metadata
- Sitemap configuration

All canonical URLs, structured-data URLs, sitemap references, and absolute links must derive from this configuration.

Do not hardcode the domain throughout the source code.

The implementation must work with any subsequently configured production domain.

Target market

Primary: United States.

Secondary: Canada and other English-speaking regions.

Primary visitors:

1. Woodworkers
2. Carpentry professionals
3. Furniture makers
4. Hardwood lumber buyers
5. Sawmill operators
6. Lumber dealers
7. DIY woodworking enthusiasts
8. Construction contractors

The site should recognize real woodworking terminology, measurement practices, and lumber-purchasing conventions.

---

2. KEYWORD RESEARCH AND SEO STRATEGY

The following keyword figures are research estimates supplied from November 2026 screenshots of Semrush.

They are planning inputs, not guarantees of search traffic.

Keyword| US monthly searches| KD
board foot calculator| 18,100| 25
how to calculate board foot| 1,600| 27
how to calculate board foot measure| 1,600| 23
log board foot calculator| 720| 6
how is board foot calculated| 480| 28
how do you calculate a board foot of lumber| 320| 23
board foot in a log calculator| 260| 7
how to calculate a board foot| 260| 17
how to calculate board foot of lumber| 260| 19
log to board foot calculator| 260| 19
lumber board foot calculator| 260| 11

The primary keyword is:

board foot calculator

Keyword targeting principles

Prioritize the primary keyword on the homepage.

Build dedicated pages only when search intent is meaningfully different.

Group search queries that can be satisfied by one authoritative page.

Avoid creating multiple nearly identical pages just to target slight keyword variations.

For example:

- "board foot calculator"
- "lumber board foot calculator"
- "calculate board feet"
- "board feet calculator"

These largely share the same user intent.

The homepage should target this cluster instead of competing against several pages on the same website.

Meanwhile, "log board foot calculator" has a different mathematical meaning and requires a dedicated calculator.

Do not deliberately optimize for branded competitor queries, including "omni board foot calculator."

Mandatory SERP research before implementation

If web access is available, examine the top organic search results for the main keyword and the highest-priority secondary keywords.

Record:

- Search intent
- Competing page types
- Calculator functionality
- Missing functionality
- Content coverage
- Formula explanations
- Units supported
- Related queries
- Relevant source references
- Common user problems

Develop a concise keyword-to-page mapping.

Do not fabricate keyword volumes, rankings, domain authority, backlinks, or competitor metrics when access to those measurements is unavailable.

Proceed using the supplied keyword data when necessary.

---

3. REQUIRED TECHNOLOGY STACK

Use:

- Astro — current stable version
- TypeScript — strict mode
- HTML5
- Native browser APIs
- Lightweight CSS integration
- "@astrojs/sitemap"
- Vitest for calculation unit tests
- Playwright for critical end-to-end tests

Do not use Next.js, Nuxt, WordPress, or a React-based single-page application.

Do not use a backend unless a feature genuinely requires one.

Do not introduce authentication, a database, or external calculation APIs.

Do not use React merely for input handling.

Astro rendering requirements

Use Astro's static output mode.

Every public, indexable page must be prerendered to actual HTML at build time.

Do not require client-side JavaScript to generate:

- Main headings
- Descriptions
- Formula explanations
- Educational sections
- Comparison tables
- FAQs
- Internal links
- Metadata
- Structured data

All those elements must already exist in the delivered HTML.

Use small, independently bundled TypeScript scripts for interactive calculator functionality.

Leverage Astro's native script bundling and tree-shaking.

Avoid client-side hydration where simple browser event listeners are sufficient.

Avoid loading unnecessary JavaScript on educational pages.

Performance requirements

Optimize for a 95–100 Lighthouse score, targeting 100 when practically achievable, in:

- Performance
- SEO
- Accessibility
- Best Practices

Core Web Vitals targets:

- LCP: 2.5 seconds or lower
- INP: 200 milliseconds or lower
- CLS: 0.1 or lower

Also establish stricter internal performance budgets wherever feasible.

Prefer:

- Zero unnecessary client-side dependencies
- Small JavaScript bundles
- Minimal network requests
- Pre-rendered content
- Local calculations
- Efficient caching
- No render-blocking third-party scripts
- No unnecessary API calls
- Efficient asset loading

Use performance measurements rather than unsupported performance claims.

---

4. PRIMARY CALCULATOR — CORE FUNCTIONALITY

The homepage must contain the primary working Board Foot Calculator.

This is the website's most important functionality.

Required inputs

- Lumber thickness
- Lumber width
- Lumber length
- Quantity of boards
- Measurement unit selection
- Price per board foot, optional
- Waste allowance percentage, optional

All values must be validated.

Support decimal and fractional measurements where appropriate.

Core board foot formula

For dimensions expressed in inches:

"Board Feet = Thickness (in) × Width (in) × Length (in) / 144"

For length expressed in feet:

"Board Feet = Thickness (in) × Width (in) × Length (ft) / 12"

For multiple identical boards:

"Total Board Feet = Board Feet Per Board × Quantity"

Example:

Thickness: 2 inches

Width: 6 inches

Length: 8 feet

Quantity: 5

Board feet per board:

"(2 × 6 × 8) / 12 = 8"

Total:

"8 × 5 = 40 board feet"

The calculator must return exactly 40 board feet for this example.

Calculation outputs

Display:

- Board feet per piece
- Total board feet
- Total board quantity
- Estimated lumber cost
- Waste allowance
- Adjusted material requirement
- Calculation breakdown
- Measurements used
- Applied pricing assumptions

The user must understand how the result was calculated.

Do not show only a number without explaining what it represents.

Real-time calculation

Calculations should update immediately after relevant input changes.

No server request should be necessary.

Avoid unnecessary computation or large runtime dependencies.

Handle all invalid-input states safely.

Examples:

- Missing dimensions
- Negative numbers
- Zero quantity
- Extremely large input
- Incorrect fraction format
- Non-numeric input
- Unreasonable waste values

Never display "NaN", "Infinity", or broken results.

Keep calculation precision separate from display formatting.

Do not round intermediate calculation results unnecessarily.

---

5. IMPORTANT LUMBER MEASUREMENT CONVENTIONS

A technically accurate woodworking calculator must distinguish nominal lumber dimensions from actual measurements.

For example, standard surfaced construction lumber commonly uses nominal dimensions such as 2×4, while its actual dimensions are approximately 1.5 × 3.5 inches.

Rough hardwood lumber can use different thickness and measurement conventions.

Therefore implement clearly separated options for:

1. Actual measured dimensions
2. Nominal dimensional lumber sizes
3. Rough hardwood thickness categories

Support thickness conventions including:

- 4/4
- 5/4
- 6/4
- 8/4
- 10/4
- 12/4

Clearly explain the relationship between quarter-inch thickness categories and their nominal rough thickness.

Example:

4/4 = 1 inch nominal rough thickness.

8/4 = 2 inches nominal rough thickness.

Do not assume rough lumber remains at its nominal thickness after surfacing.

Do not silently substitute actual dimensions for nominal dimensions.

Where a lumberyard's billing convention differs from physical measured volume, explain the difference.

A buyer should not accidentally undercalculate material costs because of an undocumented assumption.

---

6. ADVANCED CALCULATOR FEATURES

Build a practical lumber measurement utility, not a minimal multiplication form.

A. Mixed lumber tally

Allow users to add multiple board entries.

Each entry should support:

- Thickness
- Width
- Length
- Quantity
- Species label, optional
- Price per board foot, optional
- Calculated board footage
- Calculated cost

Users must be able to:

- Add entries
- Edit entries
- Duplicate entries
- Remove entries
- Clear all entries
- View a combined total

Preserve the distinction between per-board values and totals.

B. Lumber cost calculation

Formula:

"Estimated Cost = Total Board Feet × Price Per Board Foot"

Allow different board prices.

Calculate both line-item and overall totals.

Do not automatically assume material prices or market rates.

C. Waste allowance

Allow an optional waste percentage.

Make the calculation method explicit.

For example, if waste is modeled as a percentage of purchased quantity:

"Adjusted Board Feet = Required Board Feet / (1 - Waste Rate)"

Alternatively, if a user specifically chooses a percentage added to requirements:

"Adjusted Board Feet = Required Board Feet × (1 + Allowance Rate)"

These methods are not mathematically identical.

Choose a documented default, and label it accurately.

Prevent mathematically invalid values.

D. Measurement units

Support:

- Inches
- Feet
- Millimeters
- Centimeters
- Meters

Perform all conversions using consistent internal units.

Support decimal and common fraction inputs.

Show correctly converted results.

E. Shareable estimates

Provide a share function that can reproduce an estimate using a URL.

Implement compact, versioned URL state.

Validate decoded values and limit payload size.

Keep normal canonical URLs pointing to their clean page paths.

Do not create indexable duplicate pages for individual user calculations.

F. Local saving

Save the current tally in local browser storage.

Restore it when the user returns.

Handle unavailable storage without breaking the calculator.

Do not transmit saved measurements to a server.

G. Export

Support:

- CSV export
- Browser-printable estimate
- Copy result
- Copy calculation summary

CSV exports must contain usable numerical values and column headings.

Protect exported CSV from formula injection when text fields contain potentially unsafe values.

---

7. LOG BOARD FOOT CALCULATOR

Build a dedicated log calculator.

Target URL:

"/log-board-foot-calculator/"

Primary keyword:

log board foot calculator

Secondary:

- log to board foot calculator
- board foot in a log calculator
- how to calculate board feet in a log

Important:

Log scaling is not equivalent to calculating the board footage of an already-sawn rectangular board.

Use a separate calculation engine.

Initial supported log rule

Implement the Doyle log rule.

Formula:

"Board Feet = ((D - 4)² × L) / 16"

Where:

- D = small-end log diameter inside the bark, in inches
- L = log length, in feet

Document the measurement conventions.

Acknowledge that Doyle estimates are based on a log-scaling rule and are not guarantees of finished lumber yield.

Show the selected rule's name prominently in the result explanation.

Required inputs

- Small-end diameter
- Log length
- Number of logs

Required outputs

- Estimated board feet per log
- Total estimated board feet
- Calculation breakdown
- Explanation of the Doyle method
- Limitations and assumptions

Validate diameter and length.

Never produce nonsensical positive log-yield values for invalid diameters.

Important accuracy requirement

Investigate the US Forest Service's documentation on log measurement and volume estimation.

Do not invent or mix together Doyle, Scribner, and International 1/4-inch formulas.

Implement other log rules only if they can be supported by reliable references and verified calculations.

If other methods are not fully validated, publish only the Doyle implementation.

Provide a transparent explanation of why different log rules can produce different estimates.

---

8. WEBSITE STRUCTURE AND SEO LANDING PAGES

Create the following launch structure:

/
├── log-board-foot-calculator/
├── lumber-cost-calculator/
├── board-foot-chart/
├── how-to-calculate-board-feet/
├── nominal-vs-actual-lumber-size/
├── about/
├── contact/
├── privacy-policy/
├── sitemap.xml
└── robots.txt

Only publish pages containing complete, genuinely useful content or working functionality.

Do not create placeholder pages.

Homepage

URL:

"/"

Primary keyword:

board foot calculator

Target variations:

- lumber board foot calculator
- board feet calculator
- calculate board feet
- lumber board footage calculator

Suggested metadata:

Title:

"Board Foot Calculator – Calculate Lumber Board Feet Free"

Meta description:

"Free board foot calculator for lumber and woodworking. Enter thickness, width, length, and quantity to calculate board feet, lumber costs, and waste."

H1:

"Board Foot Calculator"

The homepage must include:

1. Working main calculator
2. Concise definition of a board foot
3. Formula explanation
4. Worked calculation example
5. Nominal versus actual dimensions explanation
6. Explanation of common lumber thicknesses
7. How to measure lumber accurately
8. Multiple-board calculation instructions
9. Cost estimation explanation
10. Common questions with useful answers
11. Relevant internal links

Keep the page focused on the primary user's task.

Do not bury the working calculator under long informational content.

How to Calculate Board Feet

URL:

"/how-to-calculate-board-feet/"

Primary keyword:

"how to calculate board foot"

Secondary:

- how to calculate board foot measure
- how is board foot calculated
- how do you calculate a board foot of lumber
- how to calculate a board foot
- how to calculate board foot of lumber

Suggested title:

"How to Calculate Board Feet: Formula & Examples"

This page must explain the concept thoroughly using original worked examples.

Cover:

- What a board foot represents
- Why board feet are used
- The formula
- Step-by-step measurements
- Length in inches versus feet
- Calculation for multiple boards
- Fractional measurements
- Real lumber purchasing examples
- Common mistakes
- Nominal versus actual measurements

Link prominently to the primary calculator.

Avoid duplicating all homepage content.

Log Board Foot Calculator

URL:

"/log-board-foot-calculator/"

Suggested title:

"Log Board Foot Calculator – Doyle Log Rule"

Target log-volume search intent only.

Include the actual functional log calculator and documentation of the formula.

Lumber Cost Calculator

URL:

"/lumber-cost-calculator/"

Focus on pricing and material estimation.

Users should be able to enter lumber dimensions, quantities, and board-foot prices.

Show itemized and total costs.

Ensure this page has meaningful functionality beyond a copy of the homepage.

Board Foot Chart

URL:

"/board-foot-chart/"

Create useful reference tables based on verified formulas.

Potential tables:

- Board feet for common lumber dimensions
- Board footage at different lengths
- Rough hardwood thickness reference
- Fractional thickness conversions

Generate calculations programmatically from the same calculation engine used by the calculators.

Tables must be server-rendered HTML.

Do not place essential reference data solely inside JavaScript.

Consider offering a printable reference sheet.

Verify that every table value matches the calculation engine.

Nominal vs Actual Lumber Size

URL:

"/nominal-vs-actual-lumber-size/"

Explain the distinction between lumber labels and finished physical dimensions.

Include verified dimensional lumber examples.

Explain when actual dimensions matter for computing physical volume and when suppliers bill according to nominal or rough measurements.

Include practical examples and avoid unsupported universal claims.

---

9. ON-PAGE SEO REQUIREMENTS

Every indexable page must contain:

- Unique HTML title
- Unique meta description
- Correct canonical URL
- One descriptive H1
- Logical H2/H3 hierarchy
- Relevant, natural keyword use
- Search-intent-aligned content
- Crawlable internal links
- Appropriate structured data
- Open Graph metadata
- Twitter/X card metadata
- Correct language metadata

Avoid duplicate titles and descriptions.

Keep content relevant to the page's actual functionality.

Do not generate pages merely to insert keywords.

Metadata generation

Create a reusable SEO component.

It should accept:

- Title
- Description
- Canonical path
- Page type
- Social metadata
- Indexing configuration
- Optional structured data

Generate absolute canonical URLs using the configured site URL.

Ensure canonical references are consistent with redirects and sitemap URLs.

Avoid canonicalizing different, genuinely distinct calculator pages to the homepage.

Keyword placement

Use keywords naturally in:

- Page titles
- Headings
- Relevant explanatory paragraphs
- Internal link text
- Image alternative text where appropriate
- Form labels when descriptive

Never force exact-match repetition into every paragraph.

Avoid keyword density formulas and automated keyword stuffing.

---

10. TECHNICAL SEO

Implement technical SEO as a foundational part of the application.

Crawlability

Ensure every indexable page:

- Returns HTTP 200
- Is accessible without authentication
- Exists in prerendered HTML
- Has discoverable HTML links
- Has a self-referencing canonical URL
- Is not blocked by robots.txt
- Is not marked "noindex"

Unknown routes should return an actual 404 response.

Do not turn missing pages into soft 404s.

Sitemap

Use "@astrojs/sitemap".

Generate an XML sitemap containing all canonical, indexable URLs.

Exclude:

- Error pages
- Temporary pages
- Duplicate URLs
- Search result pages
- User-specific calculation URLs
- Non-indexable utility states

Use "lastmod" only when supported by actual content modification informat
