# Tether: free test run (alpha 0.2)

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
   - "Smart App Control blocked it": see Troubleshooting below.
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
  working, the box follows the order lines on your chart. Drag its target or stop line and let go to
  replace those working orders in paperMoney with the new prices; change anything else in thinkorswim.
  To lock the box while an order is working instead, turn off "Drag target and stop to change orders"
  in Settings.

### Size

Choose Shares for a fixed number of shares, or $ at risk to size the position from the money you'd
lose if the stop is hit. "Most $ in one position" caps the size.

With more than one paperMoney account, orders go to the account selected in thinkorswim. If Tether
can't see which one that is, it picks one itself (each order names it), and Check my setup offers
Turn on: it runs thinkorswim's own switch to turn on Java accessibility for your Windows account.
Restart thinkorswim afterwards. Turn off (in the same place) undoes it. To always use one account
instead, choose it in Settings > Advanced.

### Connecting paperMoney (for paperMoney orders only)

The box works without this. You only need it to send paperMoney orders, and it needs a login
from the thinkorswim website:

1. In Tether, choose paperMoney under What to start, then click Connect paperMoney.
2. Click Copy the bookmark. Then, in your web browser, add a new bookmark and paste what you copied
   into its address (URL) box. Name it anything, like "Tether login". If you can't see your bookmarks
   bar, press Ctrl+Shift+B in Chrome or Edge to show it.
3. In that browser, log in at trade.thinkorswim.com the way you normally do, and stay on that page.
4. Click your new bookmark while you're on that page. It copies your login. (If it says to log in
   first, you're not on the logged-in thinkorswim page.)
5. Back in Tether, paste into the box and click Connect. It says Connected when paperMoney accepts it.

A login lasts at least a day and a half, and longer if you leave it alone. When it runs out, Tether says so, and you repeat steps 3 to 5 (the
bookmark is already saved).

Your login stays on your PC, in your Windows account, and is sent only to paperMoney. Treat it like
a password.


## Send feedback

This test is about three questions:

1. Did it install and run?
2. Did the box show the right prices?
3. A week from now, are you still using it?

Post your answers, and anything else you noticed, in Discussions on Tether's GitHub page:
https://github.com/SomniumDev/Tether/discussions (you need a free GitHub account). Discussions are
public, so don't include anything private. If something went wrong, open Check my setup in the
panel, click Copy diagnostics, and paste the result into your post: it's a short code that helps us find the problem.


## Troubleshooting

Smart App Control blocked Tether
: Smart App Control is a Windows 11 protection that runs a program only if Microsoft already knows it
  or it carries a paid signature, which this free test version doesn't have yet. Microsoft learns new
  programs over time, so Tether may open if you try again a day or two later. To confirm the block:
  open Event Viewer, go to Applications and Services Logs > Microsoft > Windows > CodeIntegrity >
  Operational, and look for event 3077 that names Tether.exe. Please tell us in Discussions either way.
  You don't need to turn Smart App Control off for this test.

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

In Settings > Advanced, click Uninstall Tether. It shows what will be removed, lets you keep or delete your
settings and saved paperMoney login, then closes Tether and deletes its folder and shortcuts.

To do it by hand instead:

1. In Settings, click Remove shortcuts.
2. Click Quit.
3. Delete the Tether folder.
4. To remove your settings and saved paperMoney login as well, delete the Tether folder in
   %APPDATA% (paste %APPDATA% into the File Explorer address bar to find it).


## Privacy

Tether runs on your PC. It sends nothing anywhere, except to paperMoney when you connect it
and when you send a paperMoney order. Diagnostics leave your PC only if you copy and send them
yourself. They contain your Tether settings and recent activity, never your paperMoney login or account numbers.


## Known problems and what's planned

Problems we know about:

- Tracking is poor while you move the cursor around the chart, and can lag behind the chart.
- Right after you zoom, the box can sit at the wrong prices for a moment before it corrects itself.
- **You have to reconnect paperMoney every day or two.** The saved login runs out, and connecting again
  takes a few steps (see "Connecting paperMoney" above). This only affects sending paperMoney orders;
  the box works without it.

Planned:

- **Automatic login renewal**, so you connect paperMoney once and don't have to repeat it every day. We
  haven't confirmed this is possible yet, so it's a goal, not a promise.
- Easier connecting: fewer steps when you do have to connect.

It's a free test run, so the order and timing of these depend on what testers tell us matters most.

## Who made this

Tether is an independent project by one college student (SomniumDev), built in spare time. It isn't
a company or a team, so replies and fixes may be slow. Honest feedback is what makes it better, and
it's the reason this test run exists.

## The small print

Tether is a free alpha test version from SomniumDev, provided as is, with no warranty. It isn't investment advice.
It isn't affiliated with or endorsed by Charles Schwab or thinkorswim. thinkorswim and paperMoney
are trademarks of their owners. Use it at your own risk. The open-source software it uses, and
their licences, are listed in THIRD-PARTY-NOTICES.txt.
