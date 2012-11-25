jquery.tokenpicker
========================================

You can build multi-pickable text field.

Require
------------------------------------------------------------
- jQuery 1.7+
- jQuery UI 1.8+

Options
------------------------------------------------------------
<dl>
  <dt>onPick</dt>
  <dd>
    [function] onPick callback.

    <dl>
      <dt>this</dt>
      <dd>
        [jQuery object] tokenpicker caller
      </dd>
      <dt>arguments</dt>
      <dd>
        "item" of picked (selected) item. (jQuery dom object)
      </dd>
    </dl>
  </dd>
  <dt>onRemove</dt>
  <dd>
    [function] onRemove callback.

    <dl>
      <dt>this</dt>
      <dd>
        [jQuery object] tokenpicker caller
      </dd>
      <dt>arguments</dt>
      <dd>
        "item" of picked (selected) item. (data; dom object has been removed)
      </dd>
    </dl>
  </dd>
  <dt>onSort</dt>
  <dd>
    [function] onSort callback.

    <dl>
      <dt>this</dt>
      <dd>
        [jQuery object] tokenpicker caller
      </dd>
      <dt>arguments</dt>
      <dd>
        "items" of picked (selected) items. (jQuery dom object)
      </dd>
    </dl>
  </dd>
  <dt>tokens</dt>
  <dd>
    [Arrayed Hashes][required] search tokens by hash
  </dd>
  <dt>searchKeys</dt>
  <dd>
    [Arrayed Strings][required] keys of tokens to use as search value.
  </dd>
  <dt>labelKeys</dt>
  <dd>
    [Arrayed Strings][required] keys of tokens to use as label for candidates and picked item.
  </dd>
  <dt>tokenKey</dt>
  <dd>
    [String][required] key of tokens to use as token for field value.
  </dd>
  <dt>separator</dt>
  <dd>
    [String] string for tokens joining separator. (default: comma ',' )
  </dd>
  <dt>placeholders.sort</dt>
  <dd>
    [String] placeholder text on sort. (default: 'HERE' )
  </dd>
  <dt>placeholders.start</dt>
  <dd>
    [String] placeholder text on start searching. (default: 'Type to search...' )
  </dd>
  <dt>placeholders.none</dt>
  <dd>
    [String] placeholder text on no searched result. (default: 'No Results.' )
  </dd>
</dl>

example:

    <input type="text" name="name_token" />
    <script type="text/javascript">
    <!--
    jQuery("input[name=name_token]").tokenpicker({
      onPick: function(item){
        // do something.
      },
      onRemove: function(item){
        // do something.
      },
      onSort: function(items){
        // do something.
      },
      searchKeys: [ 'name', 'company' ],
      labelKey:   'name',
      tokenKey:   'id',
      separator:  ',',
      tokens: [
        { id: 1, name: "Bob",  company: "Google" },
        { id: 2, name: "John", company: "Apple"  },
        { id: 3, name: "Mary", company: "Google" }
      ]
    });
    -->
    </script>

Utility Methods
------------------------------------------------------------
none. (please tell me if you need.)

Licence
------------------------------------------------------------
jquery.tokenpicker is licenced under the MIT License.
