#define _DEFAULT_SOURCE
#include "alloc.h"
#include <stdbool.h>
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <unistd.h>

#define HEADER_SIZE (sizeof(struct header))

int main() {
  /*
  allocopt(FIRST_FIT, 256);
  struct allocinfo info;
  void *p[11] = {NULL};
  int32_t *ptr;
  char buffer[5000];
  for (int i = 0; i < 11; i++) {
    int size = sizeof(int32_t) * 2;
    ptr = (int32_t *)alloc(size);
    if (ptr != NULL) {
      ptr[0] = 0;
      ptr[1] = 1;
      info = allocinfo();
      snprintf(buffer, sizeof(buffer), "info free size: %lu\n", info.free_size);
      write(1, buffer, strlen(buffer));
      snprintf(buffer, sizeof(buffer), "free size calc: %lu\n\n",
               INCREMENT - HEADER_SIZE - ((size + HEADER_SIZE) * (i + 1)));
      write(1, buffer, strlen(buffer));
    }
    p[i] = ptr;
  }
  for (int i = 0; i < 11; i++) {
    dealloc(p[i]); // no need for NULL check
    p[i] = NULL;
    info = allocinfo();
    snprintf(buffer, sizeof(buffer), "freeSize: %lu\n", info.free_size);
    write(1, buffer, strlen(buffer));
  }
  info = allocinfo();
  snprintf(buffer, sizeof(buffer), "freeSize: %lu\n", info.free_size);
  write(1, buffer, strlen(buffer));
  return 0;
  */

  // above has served its purpose
  allocopt(FIRST_FIT, 786);
  char *base = sbrk(0);
  void *ptr = alloc(1);
  char buffer[5000];
  snprintf(buffer, sizeof(buffer), "sbrk: %p\n", sbrk(0));
  write(1, buffer, strlen(buffer));
  snprintf(buffer, sizeof(buffer), "base + Increment: %p\n", base + INCREMENT);
  write(1, buffer, strlen(buffer));

  ptr = alloc(1);
  snprintf(buffer, sizeof(buffer), "sbrk: %p\n", sbrk(0));
  write(1, buffer, strlen(buffer));
  snprintf(buffer, sizeof(buffer), "base + Increment: %p\n", base + INCREMENT);
  write(1, buffer, strlen(buffer));

  alloc(256);
  snprintf(buffer, sizeof(buffer), "ptr: %p\n", ptr);
  write(1, buffer, strlen(buffer));
}
