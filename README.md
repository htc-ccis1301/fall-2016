<!DOCTYPE html>
<title> Student Directory </title>
<!-- based on http://git.io/vvroy -->
<div class="row">
{% assign students = site.data.fall_2016 | sort %}
{% for user_hash in students %}
{% assign username = user_hash[0] %} {% assign user = user_hash[1] %}
<div class="col-md-12 student" data-username="{{username}}">
<div class="info">
<div>
<span class="gh-username">@{{ username }}</span>
{% assign emoji = user.emoji | replace:':','' | replace:'+','--' %}
<i class="em em-{{ emoji }}"></i>
          </div>
          <div>
            <span class="name"></span>
          </div>
          <p>
            {{ user.introduction }}
          </p>
        </div>

    </div>
  {% endfor %}
</div>
