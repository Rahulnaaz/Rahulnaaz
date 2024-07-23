{exp:channel:form channel="channel9" return="Links" class="Submit" id="Submit"}
<label for="title">Title</label>
<input type="text" name="title" id="title" value="{title}" size="50" maxlength="100" onkeyup="liveUrlTitle();" />
{custom_fields}
<label for="{field_name}">{field_label}</label>
{if textarea}
<textarea id="{field_name}" name="{field_name}" dir="{text_direction}" cols="50" rows="{rows}" onclick="setFieldName(this.name)">{field_data}</textarea>
{/if}
{if textinput}
<input type="text" dir="{text_direction}" id="{field_name}" name="{field_name}" value="{field_data}" maxlength="{maxlength}" size="50" onclick="setFieldName(this.name)" />
{/if}
{/custom_fields}
{category_menu}
<label for="categories">Categories</label>
<select name="category[]" id="categories" size="4">
{select_options}
</select>
{/category_menu}
{if captcha}
<br />
<label for="captcha">Please enter the word you see in the image below:</label>
<br />
{captcha}
<br /><br />
<input type="text" name="captcha" value="{captcha_word}" maxlength="20">
{/if}
<br />
<input type="submit" name="submit" value="Submit" />
{/exp:channel:form}
