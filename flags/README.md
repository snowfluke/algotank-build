# Country flags

The country flags a tank can fly (tank/TankFlag.tsx; the list of codes is FLAG_COUNTRIES in
packages/arena/src/types.ts, and a test checks that each code has a file here). One SVG per ISO
3166-1 alpha-2 code, 4:3, from flag-icons 7.2.3 by Panayiotis Lipiridis (MIT, LICENSE.txt),
https://github.com/lipis/flag-icons. Left out: "xx" (an unknown flag) and "pc" (no country name).
To update, copy flags/4x3/??.svg of a newer release here and run the tests.
