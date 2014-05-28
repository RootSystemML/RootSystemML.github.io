---
title: beetroot
layout: default
---

[Download the rsml file](/images/examples/beeroot_1.rsml)
[Download the input image](/images/examples/beetroot_1.png)

{% highlight xml %}
<?xml version="1.0" encoding="UTF-8"?>
<rsml xmlns:po="http://www.plantontology.org/xml-dtd/po.dtd">
  <metadata>
    <version>1.0</version>
    <unit>pixel</unit>
    <resolution>1</resolution>
    <software>rhizoscan</software>
    <user/>
    <last-modified>2014-05-25T19:31:56.476235</last-modified>
    <file-key>beetroot_1</file-key>
    <image>
      <sha256>28e8aa4eff214866d3512352ace4d2528189bb2bdacf6b8d905963abfb36d061</sha256>
      <name>examples/beetroot/beetroot_1.png</name>
      <captured>2014-05-25T18:50:46</captured>
    </image>
    <time-sequence>
      <label>beetroot</label>
      <index>1</index>
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
            <point x="482.081495458" y="148.380457038" z="0"/>
            <point x="487.0" y="191.0" z="0"/>
            <point x="493.242224536" y="217.289726334" z="0"/>
            <point x="493.69696427" y="241.74379396" z="0"/>
            <point x="494.305390768" y="292.154635039" z="0"/>
            <point x="488.751590712" y="393.300140617" z="0"/>
            <point x="475.20042319" y="494.085696483" z="0"/>
            <point x="456.0" y="596.0" z="0"/>
            <point x="434.950380967" y="668.965045665" z="0"/>
            <point x="418.585152727" y="741.451671803" z="0"/>
            <point x="406.026416722" y="815.24716102" z="0"/>
            <point x="399.422636579" y="888.523875448" z="0"/>
            <point x="399.382928716" y="960.761790901" z="0"/>
            <point x="404.851038808" y="1033.79172366" z="0"/>
            <point x="424.0" y="1180.0" z="0"/>
          </polyline>
        </geometry>
        <functions>
          <function name='diameter' domain='polyline'>
            <sample>31.499979</sample>
            <sample>31.641903</sample>
            <sample>32.907166</sample>
            <sample>32.907166</sample>
            <sample>31.411253</sample>
            <sample>30.000668</sample>
            <sample>26.991653</sample>
            <sample>25.99232</sample>
            <sample>18.893604</sample>
            <sample>20.71131</sample>
            <sample>14.981135</sample>
            <sample>14.8360615</sample>
            <sample>11.865618</sample>
            <sample>11.966416</sample>
            <sample>8.975543</sample>
            <sample>7.997544</sample>
            <sample>1.0</sample>
          </function>
        </functions>
        <annotations>
          <annotation name='Free Text'>
            <point x='499.67032' y='195.35385'/>
            <value>intersection</value>
            <software>smartroot</software>
          </annotation>
          <annotation name='Free Text'>
            <point x='463.96494' y='598.08075'/>
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
              <point x="487.0" y="191.0" z="0"/>
              <point x="382.656224736" y="232.12319401" z="0"/>
              <point x="279.554469714" y="289.088656462" z="0"/>
              <point x="227.522859829" y="327.639628993" z="0"/>
              <point x="178.601717009" y="375.44093221" z="0"/>
              <point x="138.045672564" y="426.885263579" z="0"/>
              <point x="106.0" y="478.0" z="0"/>
            </polyline>
          </geometry>
          <functions>
            <function name='diameter' domain='polyline'>
              <sample>20.707533</sample>
              <sample>10.91587</sample>
              <sample>8.351888</sample>
              <sample>9.99996</sample>
              <sample>7.4624577</sample>
              <sample>5.9841623</sample>
              <sample>3.9828334</sample>
            </function>
          </functions>          
        </root>
        <root id="27" label="A" po:accession="PO:0020121">
          <properties>
            <parent-node value="9"/>
          </properties>
          <geometry>
            <polyline>
              <point x="456.0" y="596.0" z="0"/>
              <point x="486.09680018" y="612.16992136" z="0"/>
              <point x="515.519067804" y="632.715421468" z="0"/>
              <point x="571.728994944" y="686.217740442" z="0"/>
              <point x="613.521661954" y="744.727081792" z="0"/>
              <point x="629.028298111" y="773.995652423" z="0"/>
              <point x="641.0" y="802.0" z="0"/>
            </polyline>
          </geometry>
          <functions>
            <function name='diameter' domain='polyline'>
              <sample>27.363173</sample>
              <sample>10.418199</sample>
              <sample>10.418199</sample>
              <sample>8.288744</sample>
              <sample>5.914192</sample>
              <sample>5.4932504</sample>
              <sample>1.3814791</sample>
            </function>
          </functions>          
        </root>
      </root>
    </plant>
  </scene>
</rsml>
{% endhighlight %}    

