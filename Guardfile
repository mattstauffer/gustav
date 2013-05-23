# Gustav Guardfile
# To run, install the dependencies locally ( $ bundle install) and then just run Guard ( $ bundle exec guard start )

# @todo: Consider coffeescript conversion
# guard 'coffeescript', :input => 'app/assets/javascripts'

# @todo: Will this double-reload when, for example, a .js file is changed and then jammit'ed?
guard 'livereload' do
  watch(%r{.+\.(php|html|inc|md|css|scss|js)$})
end

guard :jammit,
	:config_path => "./config/assets.yml",
	:output_folder => "./assets" do
	# @todo: Is there a better way to trigger watch only dependent on assets.yml?
	watch(/.*/)
end

guard :compass do
  watch(/^source\/sass\/(.*)\.s[ac]ss/)
end
