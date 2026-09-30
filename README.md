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

<img width="1717" height="929" alt="image" src="https://github.com/user-attachments/assets/0e36a3f5-5974-4e27-ae61-1613255637e9" />
<img width="608" height="652" alt="image" src="https://github.com/user-attachments/assets/ba191b9e-74bf-4cd2-bf0b-321d0dfcbd2f" />


INSTRUCTIONS:

Option A: Installing via Compiled .dll File (Easiest) If you shared a pre-compiled .dll file, users can install it instantly without editing code:

Download the .dll file.

Open your ATAS custom indicators folder by pasting this path into your Windows File Explorer address bar: %APPDATA%\ATAS\Indicators

Drop the .dll file directly into that folder.

Open or restart ATAS, open any chart, and press Ctrl + I.

Look under the Custom category to find and add Gamma Regime (0DTE).

Option B: Visual Studio

Create a New Class Library Project Open Visual Studio and click Create a new project. Search for and select Class Library (make sure it's the C# version targeting .NET Framework or the appropriate .NET runtime version your ATAS version uses, typically .NET 10 depending on the ATAS build). Click Next.

Name your project (e.g., My Indicator), choose your saving location, and click Create.

Add ATAS Reference Assemblies To compile ATAS indicators, your project needs references to the core ATAS libraries (ATAS.Indicators.dll and OFT.Rendering.dll). In the Solution Explorer on the right, right-click on Dependencies (or References) and select Add Reference... (or Manage NuGet Packages if applicable).

Click Browse and navigate to your ATAS installation directory (usually C:\Program Files\ATAS\ or your user path).

Select the following required DLL files:

ATAS.Indicators.dll

OFT.Rendering.dll

Any other dependencies referenced by your project (like data feed cores).

Click OK to add them. (Tip: In the reference properties, set Copy Local to False since ATAS loads these natively at runtime).

Add the Code File Visual Studio automatically creates a default file named Class1.cs. Right-click it, select Rename, and change it to MyCustomIndicator.cs. Open the file, delete any placeholder code, and paste your indicator C# source code into it.

Save the file (Ctrl + S).

Build the Project Go to the top menu and select Build > Clean Solution (to clear out old build caches). Select Build > Build Solution (Ctrl + Shift + B).

Check the Output window at the bottom to ensure it says 1 succeeded, 0 failed.

Deploy to ATAS Once built successfully, go to your project folder in Windows Explorer and find the compiled file located in bin\Debug\ or bin\Release. Copy the generated .dll file.

Drop it directly into your local ATAS indicators folder: %APPDATA%\ATAS\Indicators

Open ATAS, open a chart, press Ctrl + I, and add your custom indicator from the list!

(If you have any trouble during this process, chatgpt, claude or gemini is your friend)
