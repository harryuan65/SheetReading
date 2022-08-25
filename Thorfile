require "erb"

class Default < Thor
  desc "render <template_path>", "Render erb"
  def render(template_path)
    out_path = "#{template_path.split(".").first}.html"
    template = File.read(File.expand_path(template_path))
    renderer = ERB.new(template)
    File.write(out_path, renderer.result)
  rescue => exception
    warn(exception)
  end
end
