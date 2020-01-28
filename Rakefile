# cf. GitHub - gjtorikian/html-proofer
# https://github.com/gjtorikian/html-proofer

require 'html-proofer'
task test: [:build] do
  options = {
    allow_hash_href:  true,
    check_opengraph:  true,
    check_favicon:    true,
    check_html:       true,
    disable_external: true,

    # NOTE: You can ignore file, URL, and response as follows
    #file_ignore: [
    #  /node_modules/,
    #  "./_site/PATH_TO_IGNORE_FILE
    #],
    #url_ignore:  %w(coderdojo.com linkedin.com),
    #http_status_ignore: [0, 500, 999],
  }

  HTMLProofer.check_directory('./_site', options).run
end

# Enable 'build' to flush cache files via 'clean'
task build: [:clean] do
  system 'bundle exec jekyll build'
end

task :clean do
  system 'bundle exec jekyll clean'
end
