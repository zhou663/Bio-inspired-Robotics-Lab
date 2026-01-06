 (cd "$(git rev-parse --show-toplevel)" && git apply --3way <<'EOF' 
diff --git a/README.md b/README.md
new file mode 100644
index 0000000000000000000000000000000000000000..7d69cef1a9b335a8fe927fd6a0cd5d5e03f31af9
--- /dev/null
+++ b/README.md
@@ -0,0 +1,30 @@
+# Bio-inspired Robotics Lab Website
+
+A GitHub Pages-ready Jekyll site for a robotics lab. The homepage features a hero section with a video embed, a welcome blurb, news, and research highlights. Content is powered by simple YAML data files so you can update the site without touching layouts.
+
+## Editing Content
+
+- **People:** Update `_data/people.yml` to change names, roles, bios, and photos.
+- **Publications:** Update `_data/publications.yml` to change titles, authors, venues, summaries, and tags.
+- **News:** Update `_data/news.yml` to add announcements or media coverage.
+- **Pages:** Edit `people.md`, `research.md`, `publications.md`, `equipment.md`, and `news.md` to adjust descriptions or section intros.
+- **Homepage video:** In `index.md`, replace the YouTube iframe `src` with your lab video URL.
+- **Lab logo:** Swap the hero badge/text with your logo image or add an `<img>` tag.
+
+## Local Preview
+
+GitHub Pages builds with Jekyll automatically, but you can preview locally if you have Ruby/Bundler:
+
+```bash
+bundle install
+bundle exec jekyll serve
+```
+
+Then open http://localhost:4000.
+
+## Deploying on GitHub Pages
+
+1. Push the repository to GitHub.
+2. In your repo, go to **Settings → Pages**.
+3. Set **Source** to **Deploy from a branch**, choose the **main** branch and **/ (root)** directory.
+4. Save. GitHub Pages will build the site automatically.
 
EOF
)
