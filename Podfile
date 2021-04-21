load 'build-support/dependencies.rb'

platform :ios, "11.0"

target "Amplify" do
  # Comment the next line if you"re not using Swift and don"t want to use dynamic frameworks
  use_frameworks!

  include_build_tools!

  abstract_target "AmplifyTestConfigs" do
    include_test_utilities!
    pod "AWSMobileClient", $OPTIMISTIC_AWS_SDK_VERSION
    
    target "AmplifyTestCommon" do
    end

    target "AmplifyTests" do
    end

    target "AmplifyFunctionalTests" do
    end

  end

  target "AWSPluginsCore" do
    inherit! :complete
    use_frameworks!

    pod "AWSCore", :git => 'https://github.com/ethan1022/aws-sdk-ios.git', :branch => 'main'

    abstract_target "AWSPluginsTestConfigs" do
      include_test_utilities!

      target "AWSPluginsCoreTests" do
      end

      target "AWSPluginsTestCommon" do
      end
    end

  end

end

target "AmplifyTestApp" do
  use_frameworks!
  pod "AWSMobileClient", $OPTIMISTIC_AWS_SDK_VERSION
  include_test_utilities!
end
