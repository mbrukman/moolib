
# moolib examples

To try out the A2C example locally, run

```
python examples/a2c.py
```

This produces a file called `logs.tsv` which can be plotted using
`plot.py`. To see results during training, you can run

```
watch -n3 --color python examples/plot.py logs.tsv --ykey mean_episode_return --window 500
```

in another terminal.

Here's a sample result:

```
                                mean_episode_return
  180 +---------------------------------------------------------------------+
      |           +          +           +    AAAAAAAAAAAA      +           |
  160 |-+.........:..........:..........AAAAAAA......:..........:.........+-|
      |           :          :    AAAAAAA:           :          :           |
      |           :          AAAAAA      :           :          :           |
  140 |-+.........:........AAA...........:...........:..........:.........+-|
      |           :      AAA :           :           :          :           |
  120 |-+.........AAAAAAAA...:...........:...........:..........:.........+-|
      |        AAAAA         :           :           :          :           |
      |       AA  :          :           :           :          :           |
  100 |-+....AA...:..........:...........:...........:..........:.........+-|
      |    AAA    :          :           :           :          :           |
   80 |-+.AA......:..........:...........:...........:..........:.........+-|
      |  A        :          :           :           :          :           |
      | AA        :          :           :           :          :           |
   60 |-A.........:..........:...........:...........:..........:.........+-|
      | A         :          :           :           :          :           |
   40 |AA.........:..........:...........:...........:..........:.........+-|
      |A          :          :           :           :          :           |
      |A          :          :           :           :          :           |
   20 |-+.........:..........:...........:...........:..........:.........+-|
      |           +          +           +           +          +           |
    0 +---------------------------------------------------------------------+
      0         50000      100000      150000      200000     250000      300000
                                       step
                                 logs.tsv +--A--+
```