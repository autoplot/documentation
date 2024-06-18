# 20110609: lost renderer

This was while trying to get the load order to be consistent and
correct, so that renderers are always stacked in the same order as in
the vap (except for spectrograms). This is on Jeremy's home development
environment. Note this included new code, that was not yet released.

  - load <file:/home/jbf/ct/autoplot/bugs/pw/rendererOrder3.vap>. This
    correctly shows the three panels overplotted.
  - reset. This correctly resets.
  - load <file:/home/jbf/ct/autoplot/bugs/pw/rendererOrder3.vap>. Now
    only two traces are visible. The blue trace is there--but it's
    displaying the wrong data.
  - reset. The remaining renderer has that mystery dataset there.
  - try to reset the URI. The renderer doesn't show it.

## 20110617

  - this bug still presents itself.

## 20130514

  - this bug was fixed at some point.

# 20130514

The copy plot elements down still shows one bug. I fixed a long-standing
one where the renderType would get reset, demonstrated in

```
 `<http://sarahandjeremy.net:8080/hudson/job/autoplot-test100/>` test100_Test_3pt8_CopyPlotElementsDown.png 
```
  - load
    <http://www.rbsp-ect.lanl.gov/data_prot/rbspa/rept/level3/rbspa_pre_ect-rept-sci-L3_$Y$m$d_v$(v,sep>).cdf?FEDU\&timerange=2013-02-04
  - right-click, "Plot Style"-\>Spectrogram
  - right-click, "Add Plot"-\>"Copy Plot Elements Down"

