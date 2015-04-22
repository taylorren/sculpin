---
layout: index
title: 首页 | RSYWX.com
description: RSYWX.com的首页
use: [jianshus]
---

<section class="news">
            <h1 class="section-heading text-highlight"><span class="line">简书汇编</span></h1>     
            <div class="carousel-controls">
                <a class="prev" href="#news-carousel" data-slide="prev"><i class="fa fa-caret-left"></i></a>
                <a class="next" href="#news-carousel" data-slide="next"><i class="fa fa-caret-right"></i></a>
            </div><!--//carousel-controls--> 
            <div class="section-content clearfix">
                <div id="news-carousel" class="news-carousel carousel slide">
                    <div class="carousel-inner">

                        <div class="item active"> 
{% for key, jianshu in data.jianshus|slice(0,6) %}
{% if jianshu.category is not empty %}
{% set cate=jianshu.category %}
{% else %}
{% set cate='abstract' %}
{% endif %}
                            {% include "jianshu/excerpt.html.twig" %}
                            {% if key == 2 %}
                        </div><!--//item-->
                        <div class="item"> 
                            {% endif %}
                            {% if key ==5 %}
                        </div><!--//item-->
                            {% endif %}
{% endfor %}
                    </div><!--//carousel-inner-->
                </div><!--//news-carousel-->  
            </div><!--//section-content-->     
        </section><!--//news-->
