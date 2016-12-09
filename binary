#include "stdafx.h"
#include <stdlib.h>
 
struct tree {
    int key;
    struct tree *parent, *left, *right;
    struct tree *root;
};
 
void inorder_tree_walk(struct tree *x) {
    if (x != NULL)
    {
        inorder_tree_walk(x->left);
        printf("%d ", x->key);
        inorder_tree_walk(x->right);
    }
}
 
struct tree *tree_search(struct tree *x, int key) {
    if (x == NULL || key == x->key)
        return x;
    if (key < (x->key)) {
        return tree_search(x->left, key);
    }
    else{
        return tree_search(x->right, key);
    }
}
 
struct tree *tree_minimum(struct tree *x) {
    while (x->left != NULL)
        x = x->left;
        return x;
}
 
struct tree *tree_successor(struct tree *x) {
    struct tree *y;
    if (x->right != NULL) {
        return tree_minimum(x->right);
    }
    y = x->parent;
 
        while (y != NULL && x == y->right) {
            x = y;
            y = y->parent;
            return y;
        }
}
 
struct tree *tree_insert(struct tree *x, int key) 
{
    struct tree *z = NULL;
    struct tree *y = NULL;
    x = tree->root;
    while (x != NULL)
    {
        y = x;
        if (z->key < x->key)
            x = x->left;
        else
            x = x->right;
    }
    z->parent = y;
 
    if (y == NULL)
    {
        tree->root = z;
    }
 
    else if (z->key < y->key)
        y->left = z;
 
    else
        y->right = z;
}
 
struct tree *tree_delete(struct tree *tree, int key) {
    
    struct tree *z;
    struct tree *x;
    struct tree *y;
 
    if (z->left == NULL || z->right == NULL) {
        y = z;
    }
 
    else y = tree_successor(z);
 
    if (y->left != NULL)
        x = y->left;
    else x = y->right;
 
    if (x != NULL)
        x->parent = y->parent;
 
    if (y->parent = NULL)
        tree->root = x;
 
    else if (y = y->parent->left)
        y->parent->left = x;
 
    else y->parent->right = x;
 
    if (y != z)
    z->key = y->key;
 
    return y;
}
 
int main() {
    tree *root = NULL;
    root = tree_insert(root, 7);
    root = tree_insert(root, 13);
    root = tree_insert(root, 8);
    root = tree_insert(root, 23);
    root = tree_insert(root, -7);
    root = tree_insert(root, 13);
    root = tree_insert(root, 31);
    root = tree_insert(root, 5);
    inorder_tree_walk(root);
    printf("\n\n");
 
    tree *tmp;
    tmp = tree_minimum(root);
    printf("minimum = %d\n", tmp->key);
 
    root = tree_delete(root, 8);
    root = tree_delete(root, -7);
    root = tree_delete(root, 31);
    inorder_tree_walk(root);
    printf("\n\n");
 
    tmp = tree_search(root, 13);
    if (tmp == NULL) {
        printf("no element\n");
    }
    else {
        printf("found element\n");
    }
    getchar();
}
