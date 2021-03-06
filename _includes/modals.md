## Modals

A Default Modal with a <code>.wide</code> form inside. Besides this, if you add
    <code>.center</code>
    to a modal it will be truly centered on Desktop size.

Modals are <strong>stackable</strong> (try <code>attach-image</code>) and may also replace an existing one
(try <code>?</code> next to <code>new topic</code>).
<br>
All Modals will be appended to a dedicated Container Element <code>.modal-container</code>.

<div class="showcase">
    <a class="button small secondary" data-modal="content-modal">open</a>

    <div class="modal current centered" id="content-modal">
        <i data-close-modal class="modal-close icon-cancel-1"></i>

        <h2 class="modal-title">New Topic</h2>

        <form class="wide">
            <fieldset>
                <div class="control-group">
                    <div class="multi-form break">
                        <div>
                            <label for="language_id">Language of your post</label>
                            <div class="controls">
                                <div class="select-element">
                                    <select id="language_id">
                                        <option selected>English</option>
                                        <option>German</option>
                                    </select>
                                </div>
                            </div>

                        </div>
                        <div>
                            <label for="category_id">Category</label>
                            <div class="controls">
                                <div class="select-element">
                                    <select id="category_id">
                                        <option selected>This and that</option>
                                        <option>Something else</option>
                                    </select>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </fieldset>

            <fieldset>
                <div class="control-group">
                    <label for="post_title">Topic / Headline</label>

                    <div class="controls">
                        <input id="post_title" required placeholder="Be descriptive and meaningfull"
                               maxlength="70"
                               type="text">
                    </div>
                </div>
                <div class="control-group">

                    <label for="post_content">Text</label>

                    <p>A Description may also be on top, you could write something more about
                        this here...</p>

                    <div class="controls">
                                                <textarea required
                                                          placeholder="Please be nice and do not post anything awkward"
                                                          id="post_content"></textarea>

                        <p><a  data-new-instance data-modal="async-modal"><i
                                class="icon-picture"></i>
                            attach image (launches a dedicated modal)</a></p>
                    </div>
                </div>
            </fieldset>

            <div class="form-actions">

                <div class="left">
                    <a data-close-modal class="button secondary small">Cancel</a>
                </div>

                <div class="right">
                    <button data-tooltip title="ask for help" data-modal="next-modal"
                            class="button small action secondary"><i class="icon-help"></i></button>
                    <button class="button small" type="submit">New Topic
                    </button>
                </div>
            </div>
        </form>
    </div>

</div>

<div id="next-modal" class="modal">
    <i data-close-modal class="modal-close icon-cancel-1"></i>

    <p>Post something usefull here...</p>
    <ul>
        <li>Point 1</li>
        <li>Point 2</li>
        <li>...</li>
    </ul>
    <button class="button block secondary small" data-close-modal>thanks, got it</button>
</div>
<hr>

### Alerts

<p>If you add <code>.alert</code> to a modal, it becomes a handy alert box with a fixed width. On
    smaller screens there
    will be a transition from the bottom.</p>

<div class="showcase">
    <a class="button small secondary" data-modal="second-modal">open</a>

    <div class="modal center alert current centered" id="second-modal">
        <p>Are you sure you want to delete this message?</p>

        <div class="form-actions plain">
            <div>
                <a data-close-modal class="button small secondary">no</a>
            </div>
            <div class="right">
                <a data-close-modal class="button small">yes</a>
            </div>
        </div>
    </div>
</div>
<hr>

### Minimal Markup Example

{% highlight html%}
<button data-modal="a-modal">open a modal</button>
<div id="a-modal" class="modal">
    <i data-close-modal class="modal-close icon-cancel-1"></i>
    <p>Modal-Content</p>
</div>
{% endhighlight %}

<div class="modal" id="async-modal">
    <form>
        <div class="control-group">
            <label for="file_picker">Pick a file</label>

            <div class="controls">
                <input id="file_picker" type="file"/>

                <p>Only JPEG, GIF or BMP are allowed</p>
            </div>
        </div>
        <div class="form-actions">
            <button data-close-modal class="button small">aggree, this is fun</button>
        </div>
    </form>
</div>

----

### Async

Modals may be loaded async.

<button class="button" data-modal id="AsyncModal">open an async modal</button>
