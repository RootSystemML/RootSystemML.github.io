---
title: beetroot
layout: default
---

[Download the rsml file](/images/examples/beeroot_0.rsml)

[Download the input image](/images/examples/beetroot_0.png)

{% highlight xml %}
<?xml version="1.0" encoding="UTF-8"?>
<rsml xmlns:po="http://www.plantontology.org/xml-dtd/po.dtd">
  <metadata>
    <version>1.0</version>
    <unit>pixel</unit>
    <resolution>1</resolution>
    <software>rhizoscan</software>
    <user/>
    <last-modified>2014-05-25T19:28:14.124385</last-modified>
    <file-key>beetroot_0</file-key>
    <image>
      <sha256>a32348d6ef6615ad3784f8f1bc0c7c5effe88314b99eb85189513f0532059b70</sha256>
      <name>examples/beetroot/beetroot_0.png</name>
      <captured>2014-05-25T18:51:16</captured>
    </image>
    <time-sequence>
      <label>beetroot</label>
      <index>0</index>
      <unified>true</unified>
    </time-sequence>
    <property-definitions>
      <property-definition>
        <label>parent-node</label>
        <type>integer</type>
      </property-definition>
    </property-definitions>
  </metadata>
  <scene>
    <plant id="1" label="P">
      <root id="2" label="A" po:accession="PO:0020127">
        <geometry>
          <polyline>
            <point x="467.0" y="81.5" z="0"/>
            <point x="473.0" y="105.0" z="0"/>
            <point x="482.562312938" y="148.181295917" z="0"/>
            <point x="486.5" y="191.0" z="0"/>
            <point x="493.694764548" y="211.96204905" z="0"/>
            <point x="493.261168655" y="231.99268814" z="0"/>
            <point x="494.074082386" y="271.59009049" z="0"/>
            <point x="492.497281268" y="351.551989249" z="0"/>
            <point x="473.841508393" y="510.780842562" z="0"/>
            <point x="434.363046504" y="669.145849619" z="0"/>
            <point x="403.0" y="827.0" z="0"/>
          </polyline>
        </geometry>
        <functions>
          <function name='diameter' domain='polyline'>
            <sample>27.50021</sample>
            <sample>27.965532</sample>
            <sample>28.918854</sample>
            <sample>34.306</sample>
            <sample>28.419512</sample>
            <sample>25.92708</sample>
            <sample>24.92998</sample>
            <sample>20.94123</sample>
            <sample>14.460816</sample>
            <sample>10.996638</sample>
            <sample>4.4464803</sample>
          </function>
        </functions>  
        <annotations>
          <annotation name='Free Text'>
            <point x='498.6001' y='189.25383'/>
            <value>intersection</value>
            <software>smartroot</software>
          </annotation>
        </annotations>
        <root id="14" label="A" po:accession="PO:0020121">
          <properties>
            <parent-node value="3"/>
          </properties>
          <geometry>
            <polyline>
              <point x="486.5" y="191.0" z="0"/>
              <point x="434.065917451" y="211.159138805" z="0"/>
              <point x="383.123117493" y="233.297231921" z="0"/>
              <point x="332.243288301" y="259.587349915" z="0"/>
              <point x="282.0" y="289.0" z="0"/>
            </polyline>
          </geometry>
          <functions>
            <function name='diameter' domain='polyline'>
              <sample>18.701403</sample>
              <sample>11.128505</sample>
              <sample>7.913241</sample>
              <sample>5.7337627</sample>
              <sample>4.2644463</sample>
            </function>
          </functions>          
        </root>
      </root>
    </plant>
  </scene>
</rsml>
{% endhighlight %}    

