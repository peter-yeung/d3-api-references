# d3-api-references

// 1. Selecting elements
const selection = d3.select(selector); // Or (node); https://github.com/mbostock/d3/wiki/Selections#d3_select
// Or
const selection = d3.selectAll(selector); // Or (nodes); https://github.com/mbostock/d3/wiki/Selections#d3_selectAll

// 2. Operating on selections
// 2a. Content
selection
    .attr(name[, value]) // https://github.com/mbostock/d3/wiki/Selections#attr
    .classed(name[, value]) // https://github.com/mbostock/d3/wiki/Selections#classed
    .style(name[, value[, priority]]) // https://github.com/mbostock/d3/wiki/Selections#style
    .property(name[, value]) // https://github.com/mbostock/d3/wiki/Selections#property
    .text([value]) // https://github.com/mbostock/d3/wiki/Selections#text
    .html([value]) // https://github.com/mbostock/d3/wiki/Selections#html
  .append(name) // https://github.com/mbostock/d3/wiki/Selections#append
    .insert(name[, before]) // https://github.com/mbostock/d3/wiki/Selections#insert
    .remove() // https://github.com/mbostock/d3/wiki/Selections#remove
;

// 2b. Data
selection
    .data([values[, key]]) // https://github.com/mbostock/d3/wiki/Selections#data
  .enter()[append][insert][select][call][empty][size] // https://github.com/mbostock/d3/wiki/Selections#enter
    .exit() // https://github.com/mbostock/d3/wiki/Selections#exit
    .filter(selector) // https://github.com/mbostock/d3/wiki/Selections#filter
    .datum([value]) // https://github.com/mbostock/d3/wiki/Selections#datum
    .sort([comparator]) // https://github.com/mbostock/d3/wiki/Selections#sort
    .order() // https://github.com/mbostock/d3/wiki/Selections#order
;

// 2c. Animation and interaction
selection
    .on(type[, listener[, capture]] // https://github.com/mbostock/d3/wiki/Selections#on
      d3.event // https://github.com/mbostock/d3/wiki/Selections#d3_event
      d3.mouse(container) // https://github.com/mbostock/d3/wiki/Selections#d3_mouse
        // Example

      d3.touch(container[, touches], identifier) // https://github.com/mbostock/d3/wiki/Selections#d3_touch
        // Example

      d3.touches(container[, touches]) // https://github.com/mbostock/d3/wiki/Selections#d3_touches
        // Example

    .transition([name]) // https://github.com/mbostock/d3/wiki/Selections#transition
    .interrupt([name]) // https://github.com/mbostock/d3/wiki/Selections#interrupt
;

// 2d. Subselections
selection
  .select(selector) // https://github.com/mbostock/d3/wiki/Selections#select
  .selectAll(selector) // https://github.com/mbostock/d3/wiki/Selections#selectAll
;

// 2e. Control
selection
    .each(function) // https://github.com/mbostock/d3/wiki/Selections#each
    .call(function[, arguments…]) // https://github.com/mbostock/d3/wiki/Selections#call
    .empty() // https://github.com/mbostock/d3/wiki/Selections#empty
    .node() // https://github.com/mbostock/d3/wiki/Selections#node
    .size() // https://github.com/mbostock/d3/wiki/Selections#size
;

// 2f. Extension
d3.selection(); // https://github.com/mbostock/d3/wiki/Selections#d3_selection
    // Example
    d3.selection.prototype.checked = function(value) {
      return arguments.length < 1
        ? this.property("checked")
        : this.property("checked", value);
    };
