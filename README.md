# Tether: free test run (alpha 0.1)

By SomniumDev

    THIS IS A TEST RUN ONLY.
    It's free, and it's here to find out whether traders want a tool like this.
    It isn't a finished product, and it may change or stop at any time.

    PAPERMONEY ONLY.
    It works only while thinkorswim is logged in to paperMoney.
    It can't place real-money orders: that code isn't in the program.

    ONE CHART AT A TIME.
    The box works on one chart at once. Choosing another chart moves it there.

    KNOWN ISSUES WE'RE WORKING ON
    - Poor tracking while you move the cursor around the chart
    - Laggy tracking: right after you zoom, the box can sit at the wrong prices for a
      moment before it corrects itself

Tether draws a position box on your thinkorswim chart: target, entry and stop, with your
shares, risk, reward and reward-to-risk. The box stays on its candles as you scroll and zoom. In
paperMoney you can also send the box to paperMoney as a bracket order (entry, target and stop).


## Why Windows warns you

Tether is a free test run, and it isn't code-signed. Code signing is a paid certificate that tells Windows
who published a program. Without it, Windows shows "Windows protected your PC" (or "Unknown publisher")
for any new program from a small developer. **That warning is expected.** It means Windows has no
history on the file, not that something is wrong with it.
[Microsoft explains unsigned apps here](https://support.microsoft.com/Windows/privacy/about-unsigned-apps).

To open it anyway: click "More info", then "Run anyway". If your PC has Smart App Control turned on,
Windows may block it with no option to continue. Please tell us if that happens.

## What you need

- Windows 11 or Windows 10, 64-bit
- thinkorswim desktop, logged in to paperMoney
- A chart with its price scale on the right, coloured candles and a dark colour scheme
- Display scaling of 150% or less (Settings > System > Display > Scale)

Other setups may work but haven't been tested yet. "Check my setup" (below) tells you what it finds.


## Install

1. Unzip the download anywhere you like, for example your Documents folder.
2. Open the Tether folder and double-click Tether.exe.
3. Windows may warn you, because this test version isn't signed:
   - "Windows protected your PC": click More info, then Run anyway.
   - Your antivirus may ask about it too. Allow it if you're comfortable doing so.
   - "Smart App Control blocked it": Tether can't run on that PC yet. Please tell us.
4. Read the notice that opens and click I understand.
5. To open it from the Start menu or the taskbar: Settings > Create shortcuts. Nothing starts with
   Windows: Tether runs only while its window is open.


## Use it

1. Log in to thinkorswim's paperMoney.
2. Open Tether and click Check my setup. Fix anything red.
3. Hover the mouse over a chart and press Ctrl+Alt+T. The box appears at the newest candle.
4. Drag the box:
   - the top and bottom edges set your target and stop
   - the line between the green and red parts sets your entry
   - the left and right edges change the width
   - drag anywhere else inside the box to move all of it
5. Press Ctrl+Alt+T again to remove it. Ctrl+Alt+P shows or hides the panel.

Prefer to pick the chart yourself? Click "Choose which chart to use..." in the panel. It lists the
charts it can see: hover over a row and a green frame shows which chart it is, then click the row.
If your chart isn't listed, click "Draw around a chart instead", then drag a rectangle around the
chart, like a screenshot tool (Esc cancels). Tether works on one chart at a time, so choosing a chart
while one is running moves the box there.

You can change the hotkeys in Settings.

### What to start

- Box only: just the box. Nothing can be sent.
- Dry run: the box plus an order ticket. Create order shows the order. Nothing is sent.
- paperMoney: the box plus the ticket. Create order asks paperMoney to check the order and shows
  thinkorswim's confirmation; Confirm & send places it in your paperMoney account. Once it's
  working, the box follows the order lines on your chart.

### Size

Choose Shares for a fixed number of shares, or $ at risk to size the position from the money you'd
lose if the stop is hit. "Most $ in one position" caps the size. If you have more than one
paperMoney account, enter the last 4 digits of the one to use.

### Connecting paperMoney (for paperMoney orders only)

The box works without this. To send paperMoney orders, choose paperMoney under What to start, then
click Connect paperMoney and follow the four steps in that window. A login lasts about a day: when
it runs out, Tether says so, and you repeat steps 2 to 4.

Your login stays on your PC, in your Windows account, and is sent only to paperMoney. Treat it like
a password.


## Send feedback

This test is about three questions:

1. Did it install and run?
2. Did the box show the right prices?
3. A week from now, are you still using it?

Send your answers, and anything else you noticed, to SomniumDev (the person who gave you Tether). If
something went wrong, click Copy diagnostics in the panel and paste the result into your message:
it's a short code that helps us find the problem.


## Troubleshooting

"A Windows language feature Tether needs isn't installed"
: Open Windows Settings > Time & language > Language & region. Make sure English (United States)
  is in the list (add it if not). Then click the three dots next to it > Language options, and
  install any optional features it offers. Restart Tether.

"No chart found"
: Make sure thinkorswim isn't minimised, the chart's price scale is on the right, and the chart is
  big enough to show several prices on its scale. If Choose which chart to use... lists nothing, try
  Draw around a chart instead.

The box is in the wrong place, or jumps around
: These are the known issues above. Move the chart a little and the box usually settles. Please
  send diagnostics when it happens.

Start tracking is greyed out
: thinkorswim isn't logged in to paperMoney. This test version doesn't work with live accounts.

"paperMoney login missing or expired"
: Choose paperMoney under What to start, click Connect paperMoney and paste a new login.


## Remove it

1. In Settings, click Remove shortcuts.
2. Click Quit.
3. Delete the Tether folder.
4. To remove your settings and saved paperMoney login as well, delete the Tether folder in
   %APPDATA% (paste %APPDATA% into the File Explorer address bar to find it).


## Privacy

Tether runs on your PC. It sends nothing anywhere, except to paperMoney when you connect it
and when you send a paperMoney order. Diagnostics leave your PC only if you copy and send them
yourself. They contain your Tether settings and recent activity, never your paperMoney login.


## Who made this

Tether is an independent project by one busy college student (SomniumDev), built in spare time. It isn't
a company or a team, so replies and fixes may be slow. Honest feedback is what makes it better, and
it's the reason this test run exists.

## The small print

Tether is a free alpha test version from SomniumDev, provided as is, with no warranty. It isn't investment advice.
It isn't affiliated with or endorsed by Charles Schwab or thinkorswim. thinkorswim and paperMoney
are trademarks of their owners. Use it at your own risk. The open-source software it uses, and
their licences, are listed in THIRD-PARTY-NOTICES.txt.
