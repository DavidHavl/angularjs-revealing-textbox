angular.module('App')

    .directive('revealingTextbox', function() {
        // return function (scope, element, attrs) {
        return {
            restrict: "A",
            replace: true,
            scope:{
                'label': '@',
                'title': "@",
                'placeholder': "@",
                'class': "@",
                'id': "@",
                'valmessage': '='
            },
            controller: function($scope) {
                $scope.textboxShow = false;

                $scope.toggleTextboxShow = function() {
                    if (!$scope.textboxShow && $scope.valmessage.length > 0) {
                        $scope.textboxShow = true;
                    }
                    $scope.textboxShow = !$scope.textboxShow;
                    if (!$scope.textboxShow) {
                        $scope.valmessage = '';
                    }
                }
            },
            template: '<div>' +
                          '<div class="label_wrapper">' +
                              '<input type="checkbox" data-ng-click="toggleTextboxShow()" ' +
                              'data-ng-checked="valmessage.length > 0 || textboxShow" />' +
                              '<label >{{label}}</label>' +
                              '<i class="fa fa-question-circle" title="{{title}}"></i>' +
                          '</div>' +
                          '<div class="input_wrapper" data-ng-show="valmessage.length > 0 || textboxShow">' +
                              '<input type="text" data-ng-model="valmessage" placeholder="{{placeholder}}" name="{{id}}" id="{{id}}"/>' +
                          '</div>' +
                      '</div>'
        }
    });
