Live DOM Heatmap

Overview
The Live DOM Heatmap is a high-performance, visually immersive Level 2 order book tracker built for ATAS. Rather than just displaying the current resting limit orders, it acts as a Historical Node Tracker, painting a continuous visual history of institutional liquidity. It allows you to see exactly where major walls are resting, how long they have been there, and exactly when they are pulled or filled.

Key Features
Historical Timeline Tracking: Unlike standard DOM columns, this indicator paints liquidity horizontally across time. If a large limit order is pulled or filled, the heatmap band stops exactly on that candle, leaving a permanent visual footprint of spoofing or absorption.

Dynamic Viewport Scaling: The color intensity algorithm evaluates only the liquidity currently visible on your screen. As you scroll or zoom, the colors dynamically recalibrate so the strongest wall currently in view always glows at peak intensity.

3-Layer Aesthetic Glow Engine: Levels are rendered using a 5-point color gradient combined with a 3-tier opacity model (Translucent Base, Dense Mid-Band, Opaque Hot Core) to replicate professional, studio-grade order flow visuals.

Non-Destructive UI Toggle: The on-chart toggle button allows you to instantly hide the heatmap to view raw price action. Because the data engine runs asynchronously in the background, toggling the heatmap back on instantly repaints all historical walls without missing a single tick of data.

Z-Order Background Rendering: Heatmap bands are drawn on the historical layout layer, ensuring they sit cleanly behind your candlesticks and text tags without obstructing price action.

Aggressive Memory Management: Designed for fast-moving markets, the indicator actively culls and purges invisible historical nodes that are more than 2,000 bars off-screen to keep ATAS running flawlessly.

Settings & Configuration
1. Heatmap Settings
Volume Threshold (Min Size): The minimum resting order size required to plot on the chart. Tip for NQ: Set this between 15 and 50 to filter out retail noise and only track institutional-sized limit orders.

Zone Thickness (px): Controls the vertical height of the heatmap bands.

Show Volume Tags: Toggles the numeric size tags on the right axis. Tags are only rendered for currently active, resting orders to keep the price axis clean.

Heatmap Opacity (%): A master volume knob for the transparency of the entire heatmap.

2. Aesthetic Gradient
Customize the 5-point dynamic temperature scale. By default, it interpolates smoothly from Cold to Hot:

Level 1 (Lowest): Deep Blue

Level 2: Cyan

Level 3: White Core

Level 4: Yellow/Orange

Level 5 (Max Whale Wall): Bright Red

3. UI Settings
Button Position: Anchor the toggle button to any of the four corners of your chart.

Offset X / Y: Fine-tune the pixel distance of the button from the edges of your screen.

Strategic Application
Spotting Spoofers: Watch for bright red walls that suddenly abruptly end before price reaches them. This indicates fake liquidity used to herd retail traders.

True Magnets: Walls that persist and hold their bright color as price approaches are true institutional targets or heavy defense lines. Look for price to stall or reverse violently when intersecting these historical bands.
